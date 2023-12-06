# s3-mount-ec2-linux

this repo helps you to mount s3 bucket to ec2 linux 

first update and install dependencies

```
sudo apt-get update
sudo apt install s3fs awscli -y
```

make sure install "which s3fs" command.

after that you need  IAM role to access s3 from ec2
you can give s3fullaccess. but if you want spesific you can use policy.json file on repo

after IAM role creation you need access key id and secret access key. you can use your own user or create new user.

```
echo ACCESS_KEY_ID:SECRET_ACCESS_KEY > sfs3-cred
chmod 600 s3fs-creds
```

create directory for mount s3 files. and mount command

```
mkdir s3mount
sudo s3fs <your-bucket-name> ~/s3mount -o passwd_file=~/sfs3-cred
```

and voilla
