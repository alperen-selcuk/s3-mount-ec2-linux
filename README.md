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
