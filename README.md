# Unzip-Azure-storage-Files
Automatically unzip the compressed(.zip) files whenever a file is uploaded into an Azure Storage 


# 1.Creating a Function App on VS Code (Can be created in Azure Portal too)

Clone the code from https://github.com/FBoucher/AzUnzipEverything and follow the steps given in the https://www.frankysnotes.com/2019/02/how-to-unzip-automatically-your-files.html according to your own azure settings.

![Picture1](https://user-images.githubusercontent.com/20348809/102538220-050f2b00-407a-11eb-978d-595e2a3cf4ad.png)

When the function is deployed, it unzips the file whenever a file is uploaded to the container (input container) and moves the zipped file to another container (output container). We can see the status in the logs.


# 2.	Create a Logic App in the Azure portal for moving the original data to the archive container.

![Picture1](https://user-images.githubusercontent.com/20348809/102538849-db0a3880-407a-11eb-9866-f538db652b52.png)

This is the logic app design to move the original files to the archive container

![Picture1](https://user-images.githubusercontent.com/20348809/102539188-5a980780-407b-11eb-86a6-f0b4709e4999.png)

Then use For each, within for each, you need to use Get blob content using path and Create blob.

![Picture1](https://user-images.githubusercontent.com/20348809/102539566-d85c1300-407b-11eb-9a2e-cd59bdba073e.png)
