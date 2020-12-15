# Lab 12 - Terraform Import

### 12.1

1. Create a new directory and change to it.

```shell
mkdir import_lab
cd import_lab
```

1. Create a `main.tf`.

```hcl
provider "aws" {

}

resource "aws_instance" "import" {
  # 
}
```

1. Run an `init`.

```shell
terraform init
```

1. Run a `plan`. 

Note: It will have errors about missing arguments.

```shell
terraform plan
```

### 12.2

google: terriform aws import

```shell
terraform import aws_instance.import i-1234567890
```

### 12.3

```shell
terraform show
```

### 12.4

review log

save the value of the "ami" and "instance_type" for later

### 12.5

1. Update `main.tf`.

```hcl
provider "aws" {

}

resource "aws_instance" "import" {
  ami = "yyyy"
  instance_type = "yyy"
}
```

### 12.6

1. Run a `plan`. 

```shell
terraform plan
```

1. Review log.

1. Resolve deltas ( For the lab however, do not change the tag ) until `plan` is clean.

### 12.7

1. Run an `apply`. 

```shell
terraform apply
```

1. Review log.

### 12.8

1. Run a `destroy`. 

```shell
terraform destroy
```

1. Review log.
