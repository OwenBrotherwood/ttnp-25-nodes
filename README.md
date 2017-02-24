# TTNP-25 Nodes

This repo contains the code required for various nodes attached to The Things
Network in Monmouth.

## Adding a new node type

If you want to add a new node to the system, please do the following:

   * [Fork the repo](https://github.com/ttnp-25/nodes/fork)
   * Create a new sub-directory for your node type
   * Commit your code
   * [Submit a Pull Request](https://github.com/ttnp-25/nodes/compare)

### Guidance for directory names

Obviously if everyone just started creating directories all over the place it
would be a nightmare to maintain, therefore we ask that you name your
directories for nodes as follows:

`sensors/<sensor_type>/<hardware_type>/`

So a dust sensor on an Arduino would be in a directory called `dust/arduino`,
whereas a flood sensor attached to an Intel Edison would be in `flood/edison`.

## Working on Infrastructure

The infrastructure that underpins TTNP-25 is all in source control as
Infrastructure as Code.

You can find the [Terraform](https://terraform.io) code that builds the infrastructure in the `infra/terraform`
directory and the [Ansible](https://www.ansible.com) code that configures it in the `infra/ansible` directory.

Finally, the [Packer](https://packer.io) code to build the instances is available at `infra/packer`.
