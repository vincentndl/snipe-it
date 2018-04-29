# -*- mode: ruby -*-
# vi: set ft=ruby :

SNIPEIT_SH_URL= "https://raw.githubusercontent.com/snipe/snipe-it/master/snipeit.sh"
NETWORK_BRIDGE= "en0: Wi-Fi (AirPort)"

Vagrant.configure("2") do |config|
  config.vm.define "xenial" do |xenial|
    xenial.vm.box = "ubuntu/xenial64"
    xenial.vm.hostname = 'xenial'
    xenial.vm.network "public_network", bridge: NETWORK_BRIDGE
    xenial.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    xenial.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "trusty" do |trusty|
    trusty.vm.box = "ubuntu/trusty32"
    trusty.vm.hostname = 'trusty'
    trusty.vm.network "public_network", bridge: NETWORK_BRIDGE
    trusty.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    trusty.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "centos7" do |centos7|
    centos7.vm.box = "centos/7"
    centos7.vm.hostname = 'centos7'
    centos7.vm.network "public_network", bridge: NETWORK_BRIDGE
    centos7.vm.provision :shell, :inline => "sudo yum -y update"
    centos7.vm.provision :shell, :inline => "yum install -y wget"
    centos7.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    centos7.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "centos6" do |centos6|
    centos6.vm.box = "centos/6"
    centos6.vm.hostname = 'centos6'
    centos6.vm.network "public_network", bridge: NETWORK_BRIDGE
    centos6.vm.provision :shell, :inline => "sudo yum -y update"
    centos6.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    centos6.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "jessie" do |jessie|
    jessie.vm.box = "debian/jessie64"
    jessie.vm.hostname = 'debian8'
    jessie.vm.network "public_network", bridge: NETWORK_BRIDGE
    jessie.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    jessie.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "stretch" do |stretch|
    stretch.vm.box = "debian/stretch64"
    stretch.vm.hostname = 'debian9'
    stretch.vm.network "public_network", bridge: NETWORK_BRIDGE
    stretch.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    stretch.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end

  config.vm.define "fedora25" do |fedora25|
    fedora25.vm.box = "fedora/25-cloud-base"
    fedora25.vm.hostname = 'fedora25'
    fedora25.vm.network "public_network", bridge: NETWORK_BRIDGE
    fedora25.vm.provision :shell, :inline => "dnf -y update"
    fedora25.vm.provision :shell, :inline => "dnf -y install wget"
    fedora25.vm.provision :shell, :inline => "wget #{SNIPEIT_SH_URL}"
    fedora25.vm.provision :shell, :inline => "chmod 755 snipeit.sh"
  end
end