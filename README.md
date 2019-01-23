# Prerequisiti
  
  - Istanza EC2 running
  - Bucket S3

# Procedura

  - Installa Fuse:
  
     - Debian/Ubuntu ``` sudo apt-get install s3fs ```
  
     - CentOS/RHEL ``` sudo yum install epel-release s3fs-fuse ```
                      
  - Crea il file 
  
    ``` sudo vim /etc/.passwd-s3fs ```
  
  - Inserisci in /etc/environment le credenziali di AWS: 
  
    ``` export AWSSECRETACCESSKEY=<secret_key> ```
  
    ``` export AWSACCESSKEYID=<id_key> ```
  
  - Crea il file fstab-s3 in
  
    ``` sudo vim /etc/fstab-s3 ```
  
  - Lancia il comando
  
    ``` sudo mount -aT /etc/fstab-s3 ```
