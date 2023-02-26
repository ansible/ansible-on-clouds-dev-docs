# Ansible Automation Platform on AWS minimum required IAM roles

## Foundation Roles

On top of the below roles, the user must be licensed via aws license-manager to install the desired AAP subscriptions as well.

- managed-policies
  - AWSCloudFormationReadOnlyAccess
  - AmazonS3ReadOnlyAccess
  - IAMReadOnlyAccess
  - AmazonRDSReadOnlyAccess
  - AmazonElasticFileSystemReadOnlyAccess
  - AmazonEC2FullAccess
  - AWSMarketplaceFullAccess
- cloudformation
  - cloudformation:DeleteStack
  - cloudformation:CreateUploadBucket
  - cloudformation:CreateStack
  - cloudformation:UpdateStack
- s3
  - s3:CreateBucket
  - s3:PutObject
- iam
  - iam:DetachRolePolicy
  - iam:RemoveRoleFromInstanceProfile
  - iam:DeleteInstanceProfile
  - iam:DeleteRolePolicy
  - iam:CreateRole
  - iam:PutRolePolicy
  - iam:DeleteRole
  - iam:AttachRolePolicy
  - iam:CreateInstanceProfile
  - iam:AddRoleToInstanceProfile
  - iam:PassRole
- secretsmanager
  - secretsmanager:DeleteSecret
  - secretsmanager:GetSecretValue
  - secretsmanager:GetRandomPassword
  - secretsmanager:CreateSecret
  - secretsmanager:TagResource
  - secretsmanager:PutSecretValue
- rds
  - rds:DeleteDBSubnetGroup
  - rds:DeleteDBInstance
  - rds:CreateDBSubnetGroup
  - rds:AddTagsToResource
  - rds:CreateDBInstance
- elasticfilesystem
  - elasticfilesystem:DeleteFileSystem
  - elasticfilesystem:DeleteMountTarget
  - elasticfilesystem:DeleteAccessPoint
  - elasticfilesystem:CreateFileSystem
  - elasticfilesystem:CreateAccessPoint
  - elasticfilesystem:CreateMountTarget
- sns
  - sns:ListTopics
