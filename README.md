To add betabuilder with configuration to your ios project

*   copy files into your project directory
*   cd into your project directory
*   `bundle install`
*   `cp config/betabuilder.yml.example config/betabuilder.yml`
*   edit config/betabuilder.yml
*   Test configuration (without testflight) bundle exec rake beta:archive

**Usage**
development: `bundle exec rake beta:deploy`
beta: `bundle exec rake beta:deploy env=beta`
