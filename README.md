## Run Later for Sinatra

Slight modification of [this version](https://github.com/pmamediagroup/sinatra_run_later) to clean up nicely when used through `rackup` and `ctrl-c` is sent.

## Usage:

<pre>
require 'rubygems'
require 'sinatra'
require 'run_later'

get '/' do
  run_later do
    # some task that you don't want to block.
    sleep 20
  end

  "Hello World"
end
</pre>