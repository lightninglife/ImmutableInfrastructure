<h1>Immutable Infrastructure Using Packer, Ansible, and Terraform</h1>

<h3><i>Step-by-step journal with best practice and more …</i></h3> For the project tutorial, please visit <a href="https://medium.com/paul-zhao-projects/immutable-infrastructure-using-packer-ansible-and-terraform-a275aa6e9ff7?source=friends_link&sk=9b6409cafb51dd078e2d426b7ee5abdc">here</a>.

We get started by using terraform to provision our servers and later employing ansible on instances for configuration management. This allows us to add times when provisioning servers. So that the process will not continue until configuration completes. In terms of configuration, we will be using Packer. Packer is an open source tool for creating identical machine images for multiple platforms from a single source configuration. Packer is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

<h2>Getting Started</h2>

Step 1: Setup a network using Terraform

Step 2: Create AMI using packer and ansible inside the above-created network

Step 3: Setup EC2 instance inside the network with packer AMI

Provide access key and token in Terraform and Packer code.
Command to run network Terraform

<h2>Go in folder networkTerraform, run command:</h2>
    
    terraform init
    
    terraform validate
    
    terraform apply

<h2>Command to run Packer</h2>

Provide subnet id created in network terraform in packer.json

packer build packer.json
Command to run main Terraform

<h2>Go in folder terraform, run command:</h2>

    terraform init

    terraform validate

    terraform apply

