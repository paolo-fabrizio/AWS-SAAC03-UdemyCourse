# Launch instance in Public 1A
aws ec2 run-instances --image-id ami-079db87dc4c10ac91 --instance-type t2.micro --security-group-ids sg-07cf42b5662a0238c --subnet-id subnet-07296952cda0dba3d --key-name us-east-kp --user-data file://user-data-subnet-id.txt

# Launch instance in Public 1B
aws ec2 run-instances --image-id ami-079db87dc4c10ac91 --instance-type t2.micro --security-group-ids sg-07cf42b5662a0238c --subnet-id subnet-0a17aa2e2ab3a1e40 --key-name us-east-kp --user-data file://user-data-subnet-id.txt

# Launch instance in Private 1B
aws ec2 run-instances --image-id ami-079db87dc4c10ac91 --instance-type t2.micro --security-group-ids sg-07cf42b5662a0238c --subnet-id subnet-02c502f6326e1cdcb --key-name us-east-kp --user-data file://user-data-subnet-id.txt

# Terminate instances

aws ec2 terminate-instances --instance-ids <value> <value>