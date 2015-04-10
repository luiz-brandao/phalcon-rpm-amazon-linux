# phalcon-rpm-amazon-linux
RPMs for the Phalcon PHP Framework to be installed in Amazon Linux

I am working with AWS Elastic Beanstalk and it is not always straightforward to get Phalcon installed from source using the .ebextensions configuration files. I also wanted to avoid having to install Phalcon from source everytime an instance is created, thus making the whole process faster. It my first time trying to create an RPM package, so be aware. Suggestions and improvements are welcomed.

**You gonna find the RPM inside the RPMS folder.**

- PHP5.5: php-phalcon-1.3.4-1.amzn1.5.5.x86_64.rpm
- AMI ID: aws-elasticbeanstalk-amzn-2015.03.0.x86_64-php55-hvm-201504032015 (ami-48546420)

***
### How I created the SPEC

The RPMS here might not work in your version of Amazon Linux, so I will describe how I did it so you can create one yourself if you need to. Please share it here after. 

I used a SRPM from Remi and made a few modifications so it would install on Amazon Linux. I had a hard time trying to load the macros file with the PHP variables so in the end I decided to write them directly inside the spec file. So if you are going to build a RPM, copy the values from the macros file to the spec file. The macros file for Beanstalk is probably at /usr/lib/rpm/macros.d/

I will provide precise details of how to build the RPM soon.
