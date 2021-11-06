# HW5 Message Board

**SI669 Fall 2021**

## Video Walkthrough
Please see the [Demo Video](https://www.loom.com/share/7f77adee5423485ea6c2518216a8126d). 

## Learning Goals
* Practice working with reading and writing data, especially using realtime updates, in Firebase
* Practice working with Firebase queries

## Project Goals
* Modify a Message Board app so that the user can read from and post to different "boards" within the app

## What to Do
1. Accept the GitHub Classroom invitation.
2. Clone the repo that is created to your local machine.
3. `cd` into the directory that was created when you cloned the repo (it should be called something like `si-669-hw5-message-board-<your-github-id>`).
4. Execute `npm install`
5. Implement any changes required to allow the user read from and post to the three boards already specified in the app (#general, #announcements, #random)
6. Push your final changes to GitHub before the deadline.
7. Create a screencast video and submit the link to Canvas before the deadline.
8. Indicate in your Canvas comments which requirements (including extra credit) you believe you met.

## Notes
* To get full credit, you will need to use Firebase queries (i.e., not separate collections) to select messages for each board. To support this, you can add an additional field to each message that keeps track of which board the message belongs to.
* The starter code is set up to allow the app to unsubscribe and resubscribe to the updates from the 'messageBoard' collection at any time. This allows you to change the query whose updates you are listening for.
* Remember that you can have useEffect run on every render (don't provide a second argument) or run only once (provide an empty list as the second argument). You can also have it run only when specified variables *change*. For example, `useEffect(()=>{/*function*/}, [foo])` would run after any render if and only if the value of `foo` had changed since the previous render. This information is likely to come in handy.
* You will need to cause things to happen in your app from another instance of the app, but you don't need to include video from both instances in your submission video. Just having things happen in the recorded app without any action by the current user is enough!
* Even though the starter code shows timestamps, you do not need to make the messages show in chronological order. This is actually a bit tricky (to filter AND order messages with a Firebase query), so that part is extra credit!
* The DataModel.js included with the starter code is not actually used in the app. It was left in by mistake!

## Grading (up to 120 points)
| No. | Requirement  | Points |
| --- | ------------- | ------------- |
| 1 | Messages posted to a specific board are displayed on that board | 15  |
| 2 | Messages posted to a specific board are NOT displayed on any other board | 15 |
| 3 | Messages posted to a specific board are still displayed on that board after the app reloads | 15 |
| 4 | Messages posted to a specific board are still NOT displayed on OTHER boards after the app reloads | 15 |
| 5 | Messages posted to a specific board *remotely* are shown in that board and only that board | 15 |
| 6 | Messages posted to a specific board *remotely* are still shown in the correct board after the app reloads | 15 |
| 7 | [Code Review] The code correctly uses a Firebase query to select messages to display on each board | 15 |
| 8 | [Code Review] The code correctly runs `useEffect()` when necessary, and not otherwise | 15 |
|   | **Total** | **120**

## Extra Credit

Implement a Switch that allows the user to hide/unhide completed items. Please see the Extra Credit [Demo Video](https://www.loom.com/share/ced1df9c86284c6aacc879d80f6667b1). 

## Grading (up to 4 points)
| No. | Requirement  | Points |
| --- | ------------- | ------------- |
| 1 | Messages are displayed in reverse chronological order (newest to oldest) | 1 |
| 2 | [Code Review] Code correctly uses Firebase queries to both select messages and put them in order | 3 |
|   | **Total** | **4**