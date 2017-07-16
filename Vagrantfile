# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 8200, host: 8200
  config.vm.provision "shell" do |s|
    s.inline = "apt-get update && \ 
      apt-get install unzip && \ 
      curl https://releases.hashicorp.com/consul/0.8.5/consul_0.8.5_linux_amd64.zip > consul.zip && \
      unzip consul.zip && \
      mv consul /usr/local/bin/consul && \
      curl https://releases.hashicorp.com/vault/0.7.3/vault_0.7.3_linux_amd64.zip > vault.zip && \
      unzip vault.zip && \
      mv vault /usr/local/bin/vault"
  end
end
