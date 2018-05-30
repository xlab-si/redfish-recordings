# Redfish service recordings

This repository contains selection of Redfish recordings that can be served by
the Redfish mock servers.


## Quickstart

In order to make playing with those recordings as painless as possible,
repository already contains a `Gemfile` that can be used to install
[Redfish tools gem][rf-tools] that contain mock server. Running

   [rf-tools]: https://github.com/xlab-si/redfish_tools
               (Redfish tools)

    $ bundle
    Fetching gem metadata from https://rubygems.org/...
    Resolving dependencies...
    Using bundler 1.16.1
    ...

will install Redfish tools gem with dependecies and provide `redfish serve`
command. To start serving one of the recordings (`lenovo-sr650` in this
example), we must run

    $ bundle exec redfish serve lenovo-sr650
    [2018-05-30 16:37:01] INFO  WEBrick 1.3.1
    [2018-05-30 16:37:01] INFO  ruby 2.4.3 (2017-12-14) [x86_64-linux]
    [2018-05-30 16:37:01] INFO  RedfishTools::Server#start: pid=30028 port=8000

If we now visit `localhost:8000/redfish/v1`, a healthy amount of JSON data
will fill our browser.

To terminate the server, just press `CTRL+c`.

And this is basically all there is to it.
