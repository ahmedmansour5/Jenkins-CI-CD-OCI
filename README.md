# Jenkins-CI-CD-OCI
Deploy a Jenkins CI/CD pipeline using Docker containers on Oracle Linux VM

</br>

## Reference Architecture 
The final reference architecture after the deployment and some key components are described below.

![Reference Architecture](https://github.com/ahmedmansour5/Jenkins-CI-CD-OCI/blob/main/Image/Architecture.png)

</br>

## Deployment Options
The pipeline can be deployed on [Oracle Cloud Infrastructure][oci] using the below deployment options:

1. [Terraform][tf] 
2. [Resource Manager][orm_landing] by clicking the following button  [![Deploy to Oracle Cloud][magic_button]][magic_mushop_basic_stack]

[oci]: https://cloud.oracle.com
[orm]: https://docs.cloud.oracle.com/iaas/Content/ResourceManager/Concepts/resourcemanager.htm
[tf]: https://www.terraform.io
[orm_landing]:https://www.oracle.com/cloud/systems-management/resource-manager/
[magic_button]: https://oci-resourcemanager-plugin.plugins.oci.oraclecloud.com/latest/deploy-to-oracle-cloud.svg
[magic_mushop_basic_stack]: https://cloud.oracle.com/resourcemanager/stacks/create

</br>

## Deployment Steps
The steps below guide you through deploying the pipeline on your tenancy using the OCI Resource Manager:

1. Download the [`jenkins-stack-configuration.zip`](https://github.com/ahmedmansour5/Jenkins-CI-CD-OCI/blob/main/Deployment_zip/jenkins-stack-configuration.zip) file.
2. [Login](https://cloud.oracle.com/resourcemanager/stacks/create) to Oracle Cloud Infrastructure to import the stack
    > `Home > Developer Services > Resource Manager > Stacks > Create Stack`
3. Upload the `jenkins-stack-configuration.zip` file that was downloaded earlier, and provide a name and description for the stack
4. Configure the stack
   1. **Jenkins username** - Provide a username for jenkins login
   2. **Jenkins password** - Provide a password for jenkins login
5. Review the information and click Create button.
   > The upload can take a few seconds, after which you will be taken to the newly created stack
6. On Stack details page, click on `Terraform Actions > Apply`

The private ssh key for the Linux VM will be displayed along with the public ip of the server on the Application Information tab.
