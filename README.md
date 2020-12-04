#create module for terraform go package
go mod init gopath/src/github.com/hashicorp/terraform

#download and install terraform package and dependencices

go get github.com/hashicorp/terraform/helper/schema
go get github.com/hashicorp/terraform/plugin
go get github.com/hashicorp/terraform/terraform

#build plugin using go toolchain
go build -o terraform-provider-example

The output name (-o) is very important. Terraform searches for plugins in the format of:
terraform-<TYPE>-<NAME>
