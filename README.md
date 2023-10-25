***WARNING: THIS REPO IS AN AUTO-GENERATED COPY.*** *This repo has been copied from [Gruntwork’s](https://gruntwork.io/) GitHub repositories so that you can consume it from your company’s own internal Git repositories. This copy is automatically created and updated by the `repo-copier` CLI tool. If you need to make changes to this repo, you should make the changes in a separate fork, and NOT make changes directly in this repo, as otherwise, the `repo-copier` will overwrite your changes! Please see the `repo-copier` [documentation](https://github.com/terraform-modules-krish/repo-copier) for more information on how the code is copied, how cross-references are updated, how the changelog is handled, etc.*

***

_You may find it valuable to view the following resources in the original repo. If these links give you a 404, visit https://app.gruntwork.io to gain access or email support@gruntwork.io if you need assistance._

[Home Page](https://github.com/gruntwork-io/intro-to-terraform/) |
[Pull Requests](https://github.com/gruntwork-io/intro-to-terraform/pulls) |
[Issues](https://github.com/gruntwork-io/intro-to-terraform/issues) |
[Releases and Assets](https://github.com/gruntwork-io/intro-to-terraform/releases)

_Alternatively, you can view a copied version of the resources listed above._

[Pull Requests](https://github.com/terraform-modules-krish/intro-to-terraform/blob/master/.github/PULL_REQUESTS.md) |
[Issues](https://github.com/terraform-modules-krish/intro-to-terraform/blob/master/.github/ISSUES.md) |
[ChangeLog](https://github.com/terraform-modules-krish/intro-to-terraform/blob/master/.github/CHANGELOG.md)

***

[![Maintained by Gruntwork.io](https://img.shields.io/badge/maintained%20by-gruntwork.io-%235849a6.svg)](https://gruntwork.io/?ref=repo_intro_to_terraform)
![Terraform Version](https://img.shields.io/badge/tf-%3E%3D1.1.0-blue.svg)

# NOTE: This repo is now archived and replaced!

This repo contains the sample code for the blog post series [A Comprehensive Guide to 
Terraform](https://blog.gruntwork.io/a-comprehensive-guide-to-terraform-b3d32832baca), which we turned into the 
book _[Terraform: Up & Running](https://www.terraformupandrunning.com/)_, with its own [code examples 
repo](https://github.com/brikis98/terraform-up-and-running-code). 

Instead of maintaining two examples repos, we have decided to maintain just one. This repo is now archived, so
please head over to the [terraform-up-and-running-code repo](https://github.com/brikis98/terraform-up-and-running-code) 
for the most up to date examples.

# Original content (saved for posterity)

## An Introduction to Terraform Sample Code

This repo contains the sample code for the blog post series [A Comprehensive Guide to 
Terraform](https://blog.gruntwork.io/a-comprehensive-guide-to-terraform-b3d32832baca). The examples correspond to the
following parts of the series:

1. [An Introduction to Terraform](https://blog.gruntwork.io/an-introduction-to-terraform-f17df9c6d180)
    * [single-web-server](./single-web-server): Deploy a single EC2 Instance with a web server that will return
      "Hello, World" for every request on port 8080.
    * [cluster-of-web-servers](./cluster-of-web-servers): Deploy a cluster of EC2 Instances in an Auto Scaling Group 
      (ASG) and an Elastic Load Balancer (ELB). The ELB listens on port 80 and distributes load across the EC2 
      Instances, each of which runs the same "Hello, World" web server. 
1. [How to Manage Terraform State](https://blog.gruntwork.io/how-to-manage-terraform-state-28f5697e68fa)
    * [s3-backend](./s3-backend): Create an S3 bucket and DynamoDB table to use as a Terraform backend. 
    * [database](./database): Deploy MySQL on top of Amazon's Relational Database Service (RDS). 
1. [How to create reusable infrastructure with Terraform modules](https://blog.gruntwork.io/how-to-create-reusable-infrastructure-with-terraform-modules-25526d65f73d)
    * [modules](./modules): Examples of reusable Terraform modules, including a module that can deploy a web server 
      cluster on top of ASG with an ELB. 
    * [live](./live): Examples of how to deploy different live environments (i.e., staging, production) using the code 
      from the `modules` folder. 
1. [Terraform tips & tricks: loops, if-statements, and pitfalls](https://blog.gruntwork.io/terraform-tips-tricks-loops-if-statements-and-gotchas-f739bbae55f9)
    * [loops-with-count](./loops-with-count): Examples of how to use the `count` parameters to "loop" over resources.        
    * [loops-with-for-each](./loops-with-for-each): Examples of how to use `for_each` to "loop" over inline blocks.        
    * [loops-with-for](./loops-with-for): Examples of how to use `for` to "loop" over individual values.        

## Quick start

**Note**: These examples deploy resources into your AWS account. Although all the resources should fall under the
[AWS Free Tier](https://aws.amazon.com/free/), it is not our responsibility if you are charged money for this.

1. Install [Terraform](https://www.terraform.io/).
1. Set your AWS credentials as the environment variables `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.
1. `cd` into one of the example folders.
1. Run `terraform init`.
1. Run `terraform apply`.
1. After it's done deploying, the example will output URLs or IPs you can try out.
1. To clean up and delete all resources after you're done, run `terraform destroy`.

## License

Please see [LICENSE.txt](https://github.com/terraform-modules-krish/intro-to-terraform/blob/master/LICENSE.txt) for details on how the code in this repo is licensed.
