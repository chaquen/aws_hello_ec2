# Hello EC2

This project containt an example of an api, deploy on EC2 Instance..

# How run

Type the next command:

    dotnet run

# How access from Internet

Type on your browser the url from the launchSettings.json

# How accces from SSH Client

Type in your terminal the next command

    ssh -i "Path to your key\key_pairs_mi_server.pem" ec2-user@ec2-34-236-146-226.compute-1.amazonaws.com


# Steps


1- Update your instance

    sudo yum update
    sudo yum install ruby
    sudo yum install wget
    sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
    sudo yum install aspnetcore-runtime-6.0
    dotnet --info
    cd home/ec2-user/
    wget https://aws-codedeploy-us-east-2.s3.us-east-2.amazonaws.com/latest/install
    chmod +x ./install
    sudo ./install auto
    sudo service codedeploy-agent status