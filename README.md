# Artoo Adaptor For Roomba

This repository contains the Artoo (http://artoo.io/) adaptor for the iRobot Roomba or Create robots (http://www.irobot.com/us/learn/Educators/Create.aspx).

Artoo is a open source micro-framework for robotics using Ruby.

For more information abut Artoo, check out our repo at https://github.com/hybridgroup/artoo

[![Code Climate](https://codeclimate.com/github/hybridgroup/artoo-roomba.png)](https://codeclimate.com/github/hybridgroup/artoo-roomba) [![Build Status](https://travis-ci.org/hybridgroup/artoo-roomba.png?branch=master)](https://travis-ci.org/hybridgroup/artoo-roomba)

## Installing

```
gem install artoo-roomba
```

## Using

```ruby
require 'artoo'

connection :roomba, :adaptor => :roomba, :port => '/dev/ttyUSB0'
device :roomba, :driver => :roomba, :connection => :roomba
  
work do
  roomba.safe_mode
  roomba.nudge_left
  roomba.nudge_right
  roomba.nudge_right
  roomba.nudge_left
end
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
