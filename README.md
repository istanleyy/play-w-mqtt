# Play with MQTT (derived from play-scala template)

This project experiments with Play's services to connect to a MQTT broker when application starts.
The application subscribes to topics `Lobby` and `DeviceStat` to capture messages published by
remote clients. Developers are free to define message formats to their application and implement
corresponding handlers. 

## Prerequisites

Before cloning this repo, please make sure sbt and activator are installed.
Install sbt on a Mac it's simple as 
`$ brew install sbt` or visit http://www.scala-sbt.org/download.html

To install activator go to http://www.lightbend.com/activator/download
and I recommend download the ~671M zip instead of the mini-package, unless
you are very comfortable of dealing with dependency problems ;)

After unzip activator to your directory of choice, say `/path/to/activator-x.x.x`
add it to your PATH via
```
$ export PATH=/path/to/activator-x.x.x/bin:$PATH
```
Make sure activator script is executable with
```
$ chmod u+x /path/to/activator-x.x.x/bin/activator
```

#### MQTT Server

The project connects to a local broker, mosquitto, by default. If you wish to use
another MQTT broker, please change the mqtt-broker parameters in application.conf

To get mosquitto on your machine, please visit https://mosquitto.org/download/

## Clone this project

After above is done you can clone this repo to your local folder, say play-w-mqtt,
you can then
```
$ cd play-w-mqtt
$ activator
```
to activate the Play console from the project directory.
Please checkout [Play framework documentation](https://www.playframework.com/documentation/2.5.x/Home)
to learn more about the Play console.

A quick reminder, once the Play console is activated, you should see the directory
name appear before the `$` sign in the console, i.e.,
```
[play-w-mqtt] $
```
then you can do the usual operations such as
```
[play-w-mqtt] $ test
```
to run the tests under the test folder, and then
```
[play-w-mqtt] $ compile
[play-w-mqtt] $ run
```
which are self-explanatory!


#### --- original details from template ---

This file will be packaged with your application when using `activator dist`.

#### Controllers

- Application.scala:

  Shows how to handle simple HTTP requests.

- AsyncController.scala:

  Shows how to do asynchronous programming when handling a request.

- CountController.scala:

  Shows how to inject a component into a controller and use the component when
  handling requests.

#### Components

- Module.scala:

  Shows how to use Guice to bind all the components needed by your application.

- Counter.scala:

  An example of a component that contains state, in this case a simple counter.

- ApplicationTimer.scala:

  An example of a component that starts when the application starts and stops
  when the application stops.

#### Filters

- Filters.scala:

  Creates the list of HTTP filters used by your application.

- ExampleFilter.scala

  A simple filter that adds a header to every response.