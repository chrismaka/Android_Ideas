# Android_Ideas
Ideas for android apps i intend to implement and what i have to cover to learn to implement them

This Branch the overall Idea behind Rx java.
RXJava is a library(makes it simpler) for doing reactive functional programming using java in android app development.

What is functional Reactive Programming
First, break it down.

Functional Programming
The big idea is here i mostly use methods/functions the way i would normally use variables or objects(More on this).

Reactive Programming
This involves using asynchonous(think of one way traffic, like a web page that doesn't have to reload for you to get feedback.On top making a request on this page doesn't stop you from using it while you wait for your response.)data streams. 
https://www.quora.com/What-is-difference-between-Functional-Reactive-Programming-Functional-Programming-and-Reactive-Programming.

Further more, when you think data streams, think of an actual stream of water in which the things you need to act on are floating around in barrels
https://www.quora.com/What-are-streams-in-programming.

So my general perspective of functional Reactive Programming is to have a stream in which you have things to process, and then you attach handlers/functions(functional programming type) to the streams to handle things that come flowing down the stream.

And in fact, if you think of the volley library cache dispatche or network dispatcher and its job, its similar to a stream. Both their jobs in a way is to make requests flow to places where they will be handled.

Back to RXJava.
Rx java is made of up of 3 componenents mainly and the three operate on the principle of a production line.
https://www.thedroidsonroids.com/blog/android/rxjava-production-line

Anyhow, you have the Observable-->think the production line on which things that are to be acted on flow. Click events, notification updates, location updates can all be made to run on the observable

The Observer-->this is he who consumes the things of on the observable. Think android UI/activity/service. By consuming it could mean taking that stuff running in the and putting it on the main thread which would render them on the UI.

The Operator-->think he who modifies things on the observable before the observer consumes them.

