Vagrant.configure("2") do |config|
  config.vm.define "control1" do |control1|
    control1.vm.box = "bento/ubuntu-22.04"
    control1.vm.hostname = "control"
    control1.vm.synced_folder "cka", "/cka"
    control1.vm.provider :vmware_desktop do |vmware|
        vmware.memory = 2048
    end
  end
    config.vm.define "worker1" do |worker1|
    worker1.vm.box = "bento/ubuntu-22.04"
    worker1.vm.hostname = "worker1"
    worker1.vm.synced_folder "cka", "/cka"
    worker1.vm.provider :vmware_desktop do |vmware|
        vmware.memory = 2048
    end
  end
    config.vm.define "worker2" do |worker2|
    worker2.vm.box = "bento/ubuntu-22.04"
    worker2.vm.hostname = "worker2"
    worker2.vm.synced_folder "cka", "/cka"
    worker2.vm.provider :vmware_desktop do |vmware|
        vmware.memory = 2048
    end
  end
   

end
