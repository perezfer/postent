# Postent
An events manager module to simplify the process of dispatching events to different analytics frameworks. The project is at a very early ideation phase. The objective is to elaborate a simple and elegant solution to the problem of dealing with many analytics frameworks integrated in the same software project.

# Problem definition
It is becoming more and more common to include many different analytics frameworks such as Google Analytics, Braze, Branch, Firebase ... in your app. This leads to having many places in the code where we send events in different formats, which increases code complexity and makes maintenance more difficult. Besides, having different places in the code where events are forwarded to each of the trackers increases the possibility of finding a mismatch between the data in each analytic framework.

# Solution
The idea behind the postent project is to develop a software module that simplifies handling events within the scope of a mobile app (potentially extensible to web or other platforms).
```
postent.addGoogleTracker("UA-xxxxxx-xx");
postent.addBrazeTracker("braze-id");
...
postent.sendEvent("click", eventProperties);
```
