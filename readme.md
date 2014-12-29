# Facebook Coding Challenge

Given a set of events, each with a start time and end time, render the events on a single day calendar (similar to Outlook, Calendar.app, and Google Calendar.) There are several properties of the layout:

1. No events may visually overlap.
2. If two events collide in time, they MUST have the same width. This is an invariant. Call this width W.
3. W should be the maximum value possible without breaking the previous invariant.
4. Each event is represented by a JavaScript object with a start and end attribute. The value of these attributes is the number of minutes since 9am.    So `{start:30, end:90)` represents an event from 9:30am to 10:30am. The events should be rendered in a container that is 620px wide (600px + 10px padding on the left/right) and 720px long (the day will end at 9pm). The styling of the events should match the attached screenshot.

![design](./calendar.png?raw=true)

You may structure your code however you like, but you must implement the following function in the global namespace. The function takes in an array of events and will lay out the events according to the above description.

```javascript
function layOutDay(events) {
}
```

This function will be invoked from the console for testing purposes. If it cannot be invoked, the submission will be rejected. This function should be idempotent.

In your submission, please implement the calendar with the following input:

```javascript
[ {start: 30, end: 150}, {start: 540, end: 600}, {start: 560, end: 620}, {start: 610, end: 670} ];
```

## FAQ

1. Are frameworks such as JQuery, MooTools, etc. allowed?  Yes, but please include the file with your source code.
2. Is there a maximum bound on the number of events?  You can assume a maximum of 100 events for rendering reasons, but your solution should be generalized.
3. Do I have to guard against invalid input? You may assume valid input.
4. What browsers need to be supported? Your solution should work in all modern standards-compliant browsers.
5. Does my solution need to match the image pixel for pixel? No, we will not be testing for pixel matching.
6. How will you be testing my solution? We will be running tests from the browser console by invoking the layOutDay() function. Your solution should not require a local web server (e.g. run from localhost) or have any other dependencies besides your html/css/js.
