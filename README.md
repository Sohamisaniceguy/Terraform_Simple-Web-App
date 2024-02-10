## Web-App 💻

Generic web application architecture including:
- EC2 instances
- S3 bucket
- RDS instance
- Load balancer
- Route 53 DNS config

## Architecture ⚙️
![](WebApp/architecture.png)

## Remote Backends

I have initated Remote backends to enable storage of TF state in a remote location rater than locally to enable secure collaboration.


## Notes:
- Had to add security group with IP of ec2 instance for inbound access (by default inbound traffic was blocked)
- To connect to DB (`psql -U soham123 -d mydb -p 5432 -h terraform-20210127022433201300000001.cr2ub9wmsmpg.us-east-1.rds.amazonaws.com`)
- Route 53 Configuration:
    I have mentioned a mock name for the Hosted zone name.
    To properly configure, so when the user enters the domain name in the browser the application can be accessed follow the below steps:
    1. The Domain service, Add AWS Nameservers from the Route 53 configuration.
        eg: 
        - ns-1147.awsdns-15.org
        - ns-161.awsdns-20.com
        - ns-1629.awsdns-11.co.uk
        - ns-876.awsdns-45.net

