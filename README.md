# terraform-aws-rds_cluster

```
module "aws" {
    source = ""

cluster_identifier      = "sldfjsldkfj"
  engine                  = "write your engine"
  engine_version          = "sdgdfhdfh"
  availability_zones      = var.availability_zones
  database_name           = var.database_name
  master_username         = var.master_username
  master_password         = var.master_password
# backup_retention_period = var.backup_retention_period
  preferred_backup_window = var.preferred_backup_window
  skip_final_snapshot  = true
}