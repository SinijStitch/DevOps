Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.provision "shell", inline: <<-SHELL
   cp /vagrant/filemover.service /etc/systemd/system/filemover.service
   cp /vagrant/app.sh /usr/bin/
   chmod +x /usr/bin/app.sh
   systemctl daemon-reload
   systemctl start filemover
   systemctl enable filemover.service
  SHELL
end
