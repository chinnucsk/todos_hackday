# Webmachine TODOs App #

This app showcases the [Todos](http://emberjs.com/examples/todos/) example from Ember.js using Webmachine and MySQL as backend.

The original Javascript code has been adapted to use Webmachine as backend and to be able to persist state on the server.

This project was part of a hackday at [Liip](http://www.liip.ch). The app was build by [Alvaro Videla](https://twitter.com/#!/old_sound) and [Vedran Zgela](https://twitter.com/#!/vedranzgela).

# Setup #

Simply clone the project and then run make:

    $ git clone git://github.com/videlalvaro/todos_hackday.git todos
    $ cd todos
    $ make

Then create your own configuration file by copying the sample one and then editing the MySQL configuration:

    $ cp ./priv/hackday.conf.sample ./priv/hackday.conf

# MySQL Setup #

Create the following table:

    CREATE TABLE `todo` (
      `slug` char(32) NOT NULL,
      `title` varchar(256) DEFAULT NULL,
      `isDone` tinyint(1) NOT NULL DEFAULT '0',
      PRIMARY KEY (`slug`)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8

# Running the app #

Cd into the `todos` folder and run the following command:

    $ ./start.sh

Then open [http://localhost:8000](http://localhost:8000).