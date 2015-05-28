source 'https://rubygems.org'

puppetversion = ENV.key?('PUPPET_VERSION') ? "= #{ENV['PUPPET_VERSION']}" : ['>= 3.3']
gem 'puppet', puppetversion
gem 'puppetlabs_spec_helper', '>= 0.1.0'
gem 'puppet-lint', '>= 0.3.2'
gem 'facter', '>= 1.7.0'

# RSpec-Puppet zit nog niet op RSpec 3, zie https://github.com/rodjek/rspec-puppet/pull/249
gem 'rspec-puppet', :git => 'https://github.com/electrical/rspec-puppet.git', :ref => 'rspec3'
# gem 'rspec-puppet'

group :system_test do
  # Fix voor sshd probleem bij CentOS nodesets: https://github.com/puppetlabs/beaker/pull/626
  gem 'beaker', :git => 'https://github.com/carlossg/beaker.git', :ref => 'ssh-restart', :require => false
  # gem 'beaker', '~> 2.4.0', :require => false
  gem 'beaker-rspec', '~> 5.0.0', :require => false
end
