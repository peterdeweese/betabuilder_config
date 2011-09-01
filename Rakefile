require 'rubygems'
require 'betabuilder'

BetaBuilder::Tasks.new do |config|
  yml = YAML.load_file("#{File.dirname(__FILE__)}/config/betabuilder.yml")
  yml_config = yml['default'].merge(yml[ENV['env'] || 'development'])

  config.target        = yml_config['target']
  config.app_name      = yml_config['app_name']
  config.configuration = yml_config['configuration']

  # configure deployment via TestFlight
  config.deploy_using(:testflight) do |tf|
    tf.api_token  = yml_config['api_token']
    tf.team_token = yml_config['team_token']
    tf.distribution_lists = [yml_config['distribution_list']]
    tf.notify = true
  end
end
