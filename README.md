# nclouds
I have always used saltstack for provisioning and configuration management in a cloud agnostic environments. I know linux, Networking, saltstack and python. Not a fan of Ruby :-)
 I went through all the concepts and it seems very easy to do if I use salt but might have to spend dome time on chef cook books.


1> Learnt cloud formation tried various different templates designed in designer. Some how ended up learning the I can use cloudformer tool to create a template from existing resources.

2> learned OpsWork. Using the console created stack called test and created a layer called etcd . Configured git repo for custom chef cookbooks and used community etcd cookbook. used default VPC. 
     Then used cloud former tool to create a template. could have used the etc_key resource to add the key to the etcd 

3> created a cloud formation stack using this template

4> confd 
     /etc/confd/conf.d/etcd.toml
      [template]
      src = “etcd.conf.tmpl"
      dest = "/tmp/foo”
      keys = [
          “/sandeep”,
      ]
    /etc/confd/templates/etcd.conf.tmpl
     [myconfig]
     {{getv “/sandeep”}}


