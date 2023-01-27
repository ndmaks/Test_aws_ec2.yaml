- name: start specific number of multiple instances
  amazon.aws.ec2_instance:
    instance_type: t3.small
    image_id: ami-123456
    count: 3
    region: eu-east-1
    network:
      assign_public_ip: true
      security_group: default
      vpc_subnet_id: subnet-0123456
    state: present
    tags:
      foo: bar
