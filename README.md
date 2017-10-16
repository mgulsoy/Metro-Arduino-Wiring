METRO
=====================

Metro library for Arduino or Wiring that facilitates the implementation of recurring timed events
by Thomas Ouellet Fredericks
with contributions from: Paul Bouchier and Benjamin.soelberg

Download the latest version here : https://github.com/thomasfredericks/Metro-Arduino-Wiring/archive/master.zip

Documentation can be found here : https://github.com/thomasfredericks/Metro-Arduino-Wiring/wiki

This fork adds callback ability to the original library.

<h2>Here is a usage example:</h2>

<i>Create function prototype: </i>

<code>void callback_function();</code>

<i>Create a Metro instance with the prototype: </i>

<code>Metro task1 = Metro(600, &callback_function); //ampersand should be there! </code>

<i>Insdide loop function, just call check(). It will invoke the callback</i>

<code>task1.check();</code>

<i>Don't forget to implement callback</i>

<pre>
void callback_function() {    
  //do something like:    
  Serial.println("test");
}
</pre>

