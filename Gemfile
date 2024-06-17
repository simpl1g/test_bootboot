# frozen_string_literal: true

source 'https://rubygems.org'

ruby file: '.ruby-version'

plugin 'bootboot', '~> 0.2.2'
Plugin.send(:load_plugin, 'bootboot') if Plugin.installed?('bootboot')

if ENV['DEPENDENCIES_NEXT'] == 'next'
  enable_dual_booting if Plugin.installed?('bootboot')

  # Add any gem you want here, they will be loaded only when running
  # bundler command prefixed with `DEPENDENCIES_NEXT=1`.
  gem 'rails', '7.1.3.4'
  gem 'net-protocol'
else
  gem 'rails', '7.0.8.4'
  gem 'net-protocol'
end
