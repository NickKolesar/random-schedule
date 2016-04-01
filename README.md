# random-schedule
Allows you to randomly assign events around a fixed schedule planner.

Presents the user with a weekly schedule. The user can first add fixed events to their calender as per a normal schedule planner. They can then add a number of floating random 'events' that don't allready have a fixed time. After setting up several random events with variables, the user can then click a button to randomize their floating events for the week.

This allows users to create structured schedules without creating set routines.

## Development

First step is to create a basic schedule planner. This will display an interface with the days of the week broken up by time invertvals. Allow users to set fixed points in the schedule of various lengths. And be able to save and load schedules between sessions.

* Create an interface to display the days of the week (Coloumns), and time of day (Rows)
 * Decide how time is broken up (every 60, 30, 15, 10, 5, 1 minutes?)
 * Create Schedule Data structure that can hold a number of Event data in specific time slots. (consider save/load behvario)
 * Decide how to handle conflicting events in a single time slot (Fixed Array in which each time slot can be assinged 0 or 1 events, vs Dynamic array in which events can overlap and expand)
  
* Create Events data that can be added to the schedule
 * Events should have a number of variables including Title, (fixed/floating), Duration or (Time start/Time end), Descirption/Notes, ect
 * A way to create and edit event data, either through text or interface.
  
* Create a way to interact with the scheudle to add fixed events
 * Clicking on a time, or clicking and draging over a time span should allow the user to create or edit events
 * A way to copy reoccuring events across days (i.e. sleep, job, ect)
 * A way to display the event visualy on the gui. Different presentation for fixed vs floating events.
  
* Create way to save and load schedule between sessions
 * Either a save file on the system, or using HTML5 features on web to store data locally
 * Optional: A way to save schedule templates vs assigned schedules
  
* Create way to add, edit, and display floating events
 * Floating Events should be displayed apart from the schedule (Name of event, and number of sessions)
 * Interface to add new floating event, or edit existing one
 * Floating Events should have same data as scheduled events (title, duration, fixed/floating, descirption/notes, ect), but also data such as Number of sessions, rules...
 * Optionaly: Create a way to save sets of floating events

* Create way to randomly assign floating events into the schedule...
 * Go through empty schedule and assign events, or go through unassigned events and find a free schedule?
 * Either way, make sure randomization is uniform across week. I.E. try not to stack everything on monday...
 * Prioritize condensing / simplified schedule (only on hour or half hour, rather than 5:47 ect.)
 * Deal with case: having more floating events then there is time to assign them.
