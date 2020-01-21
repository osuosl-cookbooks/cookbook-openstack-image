source 'https://supermarket.chef.io'

%w(
  client
  -common
  -identity
  -integration-test
  -ops-database
  -ops-messaging
).each do |cookbook|
  if Dir.exist?("../cookbook-openstack#{cookbook}")
    cookbook "openstack#{cookbook}", path: "../cookbook-openstack#{cookbook}"
  else
    cookbook "openstack#{cookbook}", git: "https://opendev.org/openstack/cookbook-openstack#{cookbook}"
  end
end

metadata
