# Data_mining_project
HUFS_data_mining project
#ReadMe
1. 이번 프로젝트의 ipynb파일의 경우, Google colab에서 작성되었습니다.
Google Colab에서 데이터셋을 사용하기 위해서는 자신의 구글 계정으로 구글드라이브에 csv파일을 옮기고 google colab과 연동을 시켜야 합니다.

2.Data Preprocessing 과정에서

data.drop(data[(data['Pregnancies'] > data['Pregnancies'].quantile(0.975))].index,inplace=True)
data.drop(data[(data['Glucose'] > data['Glucose'].quantile(0.975)) | (data['Glucose'] < data['Glucose'].quantile(0.025))].index,inplace=True)
data.drop(data[(data['BloodPressure'] > data['BloodPressure'].quantile(0.975)) | (data['BloodPressure'] < data['BloodPressure'].quantile(0.05))].index,inplace=True)
data.drop(data[(data['SkinThickness'] > data['SkinThickness'].quantile(0.975)) |  (data['SkinThickness'] < data['SkinThickness'].quantile(0.05))].index,inplace=True)
data.drop(data[(data['Insulin'] > data['Insulin'].quantile(0.975))].index,inplace=True)
data.drop(data[(data['BMI'] > data['BMI'].quantile(0.975)) | (data['BMI'] < data['BMI'].quantile(0.025))].index,inplace=True)
 
data.describe()

이 셀은 꼭 한번만 실행해주셔야 합니다. 제가 실행할 때 마다 상위 / 하위 값의 이상치들을 제거하는 코드로 작성하여, 여러번 실행할 경우 데이터가 계속 사라지게 됩니다.
이 셀을 실행 후 남는 데이터의 수는 1574개의 Sample이 맞습니다.
