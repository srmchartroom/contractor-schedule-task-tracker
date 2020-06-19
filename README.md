# contractor-schedule-task-tracker
This is a Javascript-based application using jQuery and Moment.js to create a runtime application for contractor developers (or really anyone) to be able to have a clean browser tab with a daily schedule tracker to help them keep track of meetings or timeblocks of work for task tracking.

## Key Functionality
The primary functionality includes:

-  **Dynamically Updated Page Header with Time up-to-the-second:** A header region that dynamically updates to the second with the current time and date.  This has a collapsible function that allows the large readout of date and additional title information to be hidden and show only the utility date, and hours:minutes:seconds and AM/PM designation.

-  **Intelligent styling for at-a-glance identification of the current, past, and future timeblocks:** The page is populated by the javascript with timeblocks that are styled according to the current time.  Previous timeblocks are styled in grey.  The current hour is in pale-red.  All future timeblocks are styled in pale-green.  At the moment that the seconds turn the hour and a new hour is started, the styles dynamically accomodate and reflect an always-up-to-date style pattern for the user to rely on.  NOTE: colors can be tweaked in javascript which has clearly commented and marked indicators for what functions do what, and where classes are being added or removed to dynamically update the color according to its relationship with the current time.

- **Persistent memory to hold values at the user- and browser-level for session independent retrieval:** Each timeblock is an input field that allows free and expandable space to write notes, meeting details, task information, or any other general information.  A click on the adjacent save icon will commit the existing entry of the text field to localStorage in the browser and remove any issues for recalling those values should the user inadvertently close the browser or computer, or have a need to recall previous hour notes after a new browser session is started.  Those localStorage memory values persist until manually cleared by the user either by removing the text data in the field and saving it, or by clearing their browser's localStorage memory key/values.  Otherwise, the user can conveniently keep track with the knowledge that their entries will be present when they hit the page again.

## Reviewing the Deployed application
You can review the deployed application at (LINK HERE)[link here].

## Potential Future Updates
In the process of building the application, obvious use cases came up. From the stance of utility as a contractor, some planned future enhancements include:

-  Inclusion of current weather and forecase details from weather api

-  Admin area to input working hours which upon submit will store the setup in localStorage and rebuild the timeblocks according to planned working hours

- Admin area to input clients which on change will dynamically update a dropdown field addition to each timeblock in which the user can select the appropriate client to which the meeting, task, or note is related.

- AutoTracker component to allow a start tracking button to capture the current time and allow the user to track time on a task.  An end tracking button would display only in the current hour and capture the end time.  The calculated time spent would be shown on the screen and save to local storage for client billing calculation.

- Totals by client/project summary section to tally all time spent on a client based on drop-down designation to provide the user with a days-end tally of time spent.

- Billable vs non-billable designator - a checkbox - to allow the user to self-categorize work as billable vs non-billable and relate it to the clients/projects.  On summary the provided tally will reflect billable time spent on a client, non-billable time spent on a client and the percent of billable time for the client or project.  This feature would also allow the user to see a total day's billable vs non-billable time to help them stay on task and ensure their work stays targeted on those tasks that result in invoiceable hours to bill.

- Multiday views.  Create a calendar for a week and month that will review the current day by default, but allow the user to select a week view of the tracker, allow the user to look at details per day via a navigation system to scroll through recorded days, and allow the user to kep track of time spent and work completed over a longer time horizon.  This would also allow for some style and set to provide print report styling (e.g. @media print) to give the user a means to print day week, and month details and summaries in a print-friendly way for long-term record-keeping and use in billing and administrative needs with clients.

- Potential integrations such as calendar integration, task app integration, etc. to pull in existing documented meetings or tasks and reflect them in your contractor to-do's and work schedule tracker.
