# Simple Crontab Calculator

A command line program to calculate the time of the next occurence of a simplified crontab.

Crontabs for the purposes of this calculator use the syntax: 

```
# ┌───────────── minute (0 - 59)
# │ ┌───────────── hour (0 - 23)
# * * script to execute
```

# To use

You require a Ruby runtime to run the script. Mac OS has ruby installed by default. Linux users will have to install ruby for continuing.

Firstly, make the script executable.
OSX 
```bash
$ chmod +x ./cron_predictor.rb
```

The program takes two arguments. The first is a time in format HH:MM and the second argument is the path to file which holds your crontabs.
```bash
./cron_predictor.rb <HH:MM> <path/to/your/input/file>
```
ex. `./cron_predictor.rb 10:20 ./example_config`

# To run specs

This project has an external dependency on `RSpec` so you will need to install this gem to run the specs. This assumes you have [bundler](https://bundler.io/) installed.

OSX
```bash
$ bundle install
$ rspec spec/*spec.rb
```
