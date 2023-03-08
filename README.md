# Quest_csharp
A gameified program that maintains a record of long term goals

## Functional Requirements
1. Provide for simple goals that can be marked complete and the user gains some value.
    * For example, if you run a marathon you get 1000 points.
3. Provide for eternal goals that are never complete, but each time the user records them, they gain some value.
    * For example, every time you read your scriptures you get 100 points.
5. Provide for a checklist goal that must be accomplished a certain number of times to be complete. Each time the user records this goal they gain some value, but when they achieve the desired amount, they get an extra bonus.
    * For example, if you set a goal to attend the temple 10 times, you might get 50 points each time you go, and then a bonus of 500 points on the 10th time.
7. Display the user's score.
8. Allow the user to create new goals of any type.
9. Allow the user to record an event (meaning they have accomplished a goal and should receive points).
10. Show a list of the goals. This list should show indicate whether the goal has been completed or not (for example [ ] compared to [X]), and for checklist goals it should show how many times the goal has been completed (for example Completed 2/5 times).
11. Allow the user's goals and their current score to be saved and loaded.

## Design Requirements
1. Use inheritance by having a separate class for each kind of activity with a base class to contain any shared attributes or behaviors.
2. Use polymorphism by having derived classes override base class methods where appropriate.
3. Follow the principles of encapsulation and abstraction by having private member variables and putting related items in the same class.

### 5 classes?
* Goal: to keep track of progress
    * Attributes: string name, string description, int points
    * Methods: Goal(name, desc, points), string getName(), string getDesc(), int getPoints(), void recordProgress(), bool isComplete()
* Simple, Eternal, and Checklist
* Goal Repo: to keep track of goals
    * Attributes: List<strings> goalList
    * Methods: string Add(), void Remove(), List<string> getAll()
* Text Goal Repo, Json Goal Repo
* Command: handles user input
    * Method: void Execute(),
    * Inheirit: Add, Remove, Update Goal, View progress, View Menu