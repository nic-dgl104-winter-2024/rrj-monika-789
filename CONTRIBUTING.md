# Open Source Project Contribution: 

## Part 1: Assess External Communitie Contribution :


## Project Name: Rock-Paper-Scissors-Game

This project aims to create a responsive Rock, Paper, Scissors game using HTML, CSS, and JavaScript. HTML will structure the game layout, CSS will style it for visual appeal 
and responsiveness, and JavaScript will handle player input and game logic. This classic game will be enjoyable on any device, providing entertainment for users of all ages.

### Key Feaures:

Responsive Design: The game interface is designed to be responsive, ensuring a seamless experience across various devices and screen sizes.
Score Tracking: The game keeps track of the player's and computer's scores, updating them dynamically with each round.
Randomized Computer Choice: The computer's choice (rock, paper, or scissors) is generated randomly for each round, adding unpredictability to the game.
Reset Functionality: A reset button allows the player to reset the game, clearing scores and resetting hand images to their initial state.
Animation: The game features animation effects (shake) to provide an engaging and interactive experience when the player and computer make their choices.


### Link:

https://github.com/monika-789/rock-paper-scissors-game/tree/monika-dev-game


### Summary of issues examined:

The issue identified is that when the buttons are rapidly clicked, multiple inputs can be registered for subsequent rounds before the current round is resolved.
This can lead to unexpected behavior and disrupt the flow of the game.


### Detailed discussion of issues contributed to:

I worked on a specific issue related to preventing multiple button clicks in my Rock, Paper, Scissors game. I explored different methods, including using the disabled attribute of HTML
buttons and adding/removing event listeners.I found a solution by immediately disabling the buttons after a player makes a selection and re-enabling them after displaying
the round outcome. This approach ensured that only one round is processed at a time, preventing confusion and unexpected results. I also looked into other websites and tutorials such
as MDN Web Docs and Stack Overflow to gather insights and examples on how to handle button clicks and prevent multiple selections in JavaScript.


The solution involves two functions: disableButton() and ResetButtonsState().

In the disableButton() function, the buttons for rock, paper, and scissors are disabled immediately after a player makes a selection. This prevents the player from clicking them
again until the current round is resolved. The function retrieves the button elements by their IDs and sets their disabled property to true, effectively disabling them.

The ResetButtonsState() function is responsible for re-enabling the buttons after the outcome of the round is displayed and the game resets. This function retrieves the button
elements again and sets their disabled property back to false, allowing the player to make selections for the next round.

Together, these functions ensure that only one selection can be made at a time, preventing multiple button clicks and ensuring a smoother gameplay experience for the player.


### Code:

#### app.js:

Updated solution code
```
 // enable buttons again
  ResetButtonsState();
```
```

/* Disable button untill */
function disableButton() {

  // Get the button element by its ID
  var rockBtn = document.getElementById("rockButton");
  var paperBtn = document.getElementById("paperButton");
  var scissorBtn = document.getElementById("scissorButton");

  // Disable the button
  rockBtn.disabled = true;
  paperBtn.disabled = true;
  scissorBtn.disabled = true;
}

function ResetButtonsState()
{
  var rockBtn = document.getElementById("rockButton");
  var paperBtn = document.getElementById("paperButton");
  var scissorBtn = document.getElementById("scissorButton");

  // Disable the button
  rockBtn.disabled = false;
  paperBtn.disabled = false;
  scissorBtn.disabled = false;
}
```


### Code review and Outcomes:

After receiving feedback from a classmate during a code review, it was pointed out that the comment stating "// Disable the button" appeared to be inaccurate as the subsequent code sets the disabled property of each button to false, effectively enabling the buttons instead of disabling them. As a result of this feedback, adjustments were likely made to the comment to accurately reflect the code's behavior. Additionally, the suggestion to include code changes directly from the .js file in a pull request (PR) was likely implemented, simplifying the code review process and enabling clearer communication among collaborators. Overall, the feedback contributed to improved accuracy and efficiency in code documentation and review practices.


### Reflection:

Upon reflection, the issue of preventing multiple button clicks was successfully resolved. Initially, the game experienced the problem of processing multiple rounds simultaneously
when players clicked buttons rapidly, leading to confusion and unexpected outcomes. The roadblock faced was finding an effective way to disable the buttons temporarily after a
player's selection until the current round was resolved. This was overcome by implementing the disableButton() function to disable the buttons immediately after a click, preventing
additional selections until the current round was completed. Additionally, the ResetButtonsState() function ensured that the buttons were re-enabled after the round outcome was
displayed, allowing for subsequent rounds to proceed smoothly. Through careful implementation and testing, the solution effectively addressed the issue, resulting in a more controlled
and enjoyable gameplay experience for players.


### Discussion of next steps:

The next step is to conduct thorough testing of the button disabling functionality to ensure it works reliably across different scenarios and devices. Gathering feedback from users
will provide valuable insights into any usability issues or areas for improvement. Additionally, documenting the implemented solution will serve as a reference for future development
and maintenance. Finally, considering potential enhancements to further improve the gameplay experience, based on user feedback and project requirements, will be essential for the
game's continued success.


### Reference:

* [MDN Web Docs] (https://developer.mozilla.org/en-US/docs/Web)
* [Stack Overflow] (https://stackoverflow.com/)






## Part 2: pattern Library Contribution :

### Read through pattern library issues:

I engaged in an activity during our class where I reviewed all the available issues in the repository and decided to pursue the Lua implementation for the Observer pattern (#13). Since I aimed to explore a new programming language, this issue seemed ideal for me to undertake. I made a comment on the issue titled 'Add Lua implementation for Observer pattern #13' and requested to assign it to myself. My intention was to independently write code and develop a small project to demonstrate and explain the fundamental concepts of Lua. Upon completion, I submitted a pull request.


### Contribute to Pattern-library:

I began contributing to the Pattern-library project by tackling an assigned issue focused on implementing and explaining the Observer pattern in Lua. To start, I created a copy of the pattern-library repository called a 'fork.' You can find my fork [here](https://github.com/monika-789/pattern-library/tree/Monika-dev-branch/patterns/Behavioral/Observal/Lua). Since Lua's Observer pattern was new to me, I researched online and found helpful references to understand it better. For my demonstration, I decided to write code for a simple project using the GameSubject example. After completing the code, I submitted my first pull request (PR) for review.


### Code Review:

I received some helpful feedback. They suggested adding more comments at the top of methods to explain their intended behavior, especially for those new to the pattern. Additionally, they recommended removing unnecessary print statements to avoid confusion and clutter in the code. To improve clarity in the score function, it was suggested to include the subject's name in the update message. There was also a question about the use of __index, prompting a need for further explanation. They advised separating the notify function from updateScore and suggested triggering notify on state updates to reflect changes, which may in turn call updateScore as needed. Lastly, they appreciated the existing comments and suggested adding similar ones to enhance understanding throughout the code. 

Following the implementation of these changes, I submitted another pull request, which was promptly accepted and merged into the main repository. This signifies that the feedback provided by my classmates was beneficial in improving the quality of the code. 


### Reflections:

Initially, I expressed my interest in contributing to the project and was tasked with researching and implementing the Observer pattern in Lua. My focus was on understanding the principles and basic coding required for this pattern. After familiarizing myself with tutorials and documentation, I submitted a pull request to integrate my findings into the main pattern library repository. One of the major struggles I faced was finding suitable resources online, but thorough research helped me understand the concept comfortably. The initial code I submitted was a basic game subject code, which underwent refinement through code reviews to improve its quality. This experience underscores the value of working together, continuous learning, and being open to feedback in this assignment.


### References:

* Lua users wiki (https://lua-users.org/wiki/)
* Stack Overflow (https://stackoverflow.com/)





