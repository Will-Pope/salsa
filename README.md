Salsa
=====

Styled and Accessible Learning Service Agreements

Visit [syllabustool.com](http://syllabustool.com) for more information

Development Installation Notes (Rough Cuts)
-------------------------------------------

Requires Ruby 1.9+, Rails 4.0+

(2.0.0-p481 works with the debugger gem, the latest didn't)

Clone repository

    git clone https://github.com/idbygeorge/salsa.git
    cd salsa

Copy `config/database.yml.default` paste to `config/database.yml`, change as necessary.

Copy `config/config.yml.default` paste to `config/config.yml`, change as necessary.

    bundle install
    rake db:create
    rake db:migrate

To run the server, from the project root type:

    rails server

Goto [http://localhost:3000](http://localhost:3000) (ctrl + c shutsdown the server)

Production Notes
----------------

* OS: Ubuntu 12.04
* Web server: nginx, unicorn
* Database: PostgreSQL

Deploy through Capistrano

Copy `config/deploy/production.rb.default` paste to `config/deploy/production.rb`, change as necessary.

    cap production deploy
