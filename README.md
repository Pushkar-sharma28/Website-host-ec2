### Website link:

[https://www.free-css.com/free-css-templates/page290/brainwave](https://www.free-css.com/free-css-templates/page290/brainwave)

### Steps

- Make an EC2 instance
- Install Apache web server on it
- Download files for the website from the above link or simply clone this repo
- Copy all the files to `var/www/html`
- Set up the Apache web server

### Making EC2 instance:
![image](https://github.com/Pushkar-sharma28/Website-host-ec2/assets/108188779/a36f50a1-af36-4177-866a-200aa5c50833)


### Setting up the website:

- Downloading the website from the link
```
wget https://www.free-css.com/assets/files/free-css-templates/download/page290/brainwave.zip
unzip brainwave.zip
ls
```   
- Installing Apache web server and checking its status
```
yum install httpd
service httpd status

```

- Moving files from the unzipped folder to /var/www/html because all the files are going to be hosted from there with the help of Apache server

```
cd brainwave-html
ls
mv * /var/www/html/
cd /var/www/html
```

- Starting the web server so that our website can be hosted
```
service httpd status
service httpd start

```
- Copy paste the public ip of instance to your browser take care of the security groups of the instance i.e. https requests should be enabled for the server

![Screenshot (64)](https://github.com/Pushkar-sharma28/Website-host-ec2/assets/108188779/42e7b614-dfe3-4cd0-9690-f76e01912f60)
