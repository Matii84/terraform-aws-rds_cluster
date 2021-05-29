# terraform-aws-rds_cluster
 ## Please use below code

```
 module "rds_cluster" {
  source  = "Matii84/rds_cluster/aws"
  
resource "aws_rds_cluster_instance" "cluster_instances" {
  count              = 2
  identifier         = var.cluster_identifier
  cluster_identifier = var.cluster_identifier
  instance_class     = "db.r4.large"
  engine             = var.engine
  engine_version     = var.engine_version
  
} 
  cluster_identifier      = "aurora-cluster-demo"
  engine                  = "aurora-mysql"
  engine_version          = "5.7.mysql_aurora.2.07.2"
  availability_zones      = ["us-east-2a", "us-east-2b", "us-east-2c"]
  database_name           = "db"
  master_username         = "foo"
  master_password         = "MYPROJECT"
  preferred_backup_window = "07:00-09:00"
  skip_final_snapshot  = true
  region = "us-east-2" 
  subnet_ids = ["subnet-05d8f5c18eb5835cc","subnet-0c318d56b15a0b068","subnet-072d5daecb76219cc"]
}
```
