<sub>[Back to README](../../README.md)</sub>

[日本語](./sg_ja.md) | [English](./sg_en.md)

# Storing Groceries (SG)

Reference Video: https://www.youtube.com/watch?v=gzdSRsNC25s

> [!NOTE]  
> This video shows a competition from the past. The rules may differ from the current competition.


The robot stores groceries in a cabinet with shelves. Objects are sorted on the shelves based on similarity, for instance, an apple is stored next to other fruits.

**Main goal:** Move objects from a table to the cabinet, grouping them by category or similarity. Refill the cereal container.

**Optional goals**
<!-- 1. Opening the cabinet doors -->
1. Moving a tiny object
1. Moving a heavy object
1. Picking up objects from the shopping bag

### Focus
Object detection and recognition, object feature recognition, object manipulation.

### Setup
* **Locations:**
    * **Start location:** Before the test, the robot waits outside the arena and navigates to the testing area when the door is open.
    * **Test location:** The testing area has a cabinet and a table nearby.
* **People:**
    * No people are involved in the test, unless the robot requires human assistance.
* **Furniture:**
    * **Table:** The table has 5–10 objects placed on it, and the robot can choose which ones to grasp and in what order. On smaller tables, new objects will be added as the robot frees up space.
    * **Shopping Bag:** A shopping bag with 5–10 additional items is placed on the ground next to the table.
    * **Cabinet:** The cabinet contains objects arranged in groups — either by category or similarity — on different shelves.
    <!-- * **Cabinet door:** The cabinet is initially closed. If the robot cannot open the door, it must clearly request assistance from the referee. -->
* **Objects**:
    * **Table objects:** The objects on the table are arranged arbitrarily.
    <!-- * **Cabinet objects:** The objects are placed behind the cabinet doors and cannot be accessed unless the doors are open. -->
    * **Cabinet objects:** The objects are placed in the cabinet.
    * **Containers:** The container for the cornflakes is placed on the table.
    <!-- * **Containers:** The container for nori (seaweed) is placed on the table. (Japanese version) -->

### Procedure
1.  **Table location:** On Setup Day, the OC/TC will announce which table and cabinet will be used in the test, along with the approximate table location.
2.  **Test start:** The robot enters the testing area once the arena door is opened.
3.  **Storing groceries:** After identifying the table, the robot moves the objects from the table to the cabinet.
4.  **Pouring cereal:** The robot pours cereal into the designated open container.
<!-- 4.  **Pouring dried seaweed:** The robot pours dried seaweed into the designated open container. (Japanese version) -->

### Additional rules and remarks
1.  **Table:** The approximate location of the table will be announced in advance, and it will be positioned near the cabinet.
2.  **Incorrect categorization:** The score is reduced if an object is stored in the cabinet but not on a shelf with similar objects; this reduction is applied per incorrectly stored object.
3.  **New category:** Objects that do not belong to any of the categories on the shelves should be grouped together on a new shelf.
4.  **Deus Ex Machina:** Scores are reduced if human assistance is received, in particular for:
    * telling or pointing out to the robot where to place an object
    * moving an object instead of the robot
    <!-- * opening the cabinet doors -->
5.  **Communicating Perception**: The robot must clearly communicate its perception to the OC/TC.
    Pointing at the object or attempting to pick it up is sufficient.
    If using a visual UI, the robot must indicate where the OC/TC should look and ensure the display is clearly accessible.
    If the team wants to utilize bounding boxes, make sure **only** one object with a bounding box is shown at a time, so the OC/TC can easily check and verify.
    The surrounding scene must also be visible; cropped views alone are insufficient.

### Score sheet

**Time Limit:** 7 minutes

| Action | Points | Max Repetitions |
| :--- | :--- | :--- |
| **Main Goal** |
| &emsp; - Navigating to the table | 15 | 1 |
| &emsp; - Perceiving object and categorizing it correctly | 15 | 5 |
| &emsp; - Picking up an object for transportation to the cabinet | 50 | 5 |
| &emsp; - Perceiving objects in shelf and saying where to place object | 15 | 5 |
| &emsp; - Placing an object in the cabinet | 15 | 5 |
| &emsp; - Placing an object next to similar objects on the cabinet | 50 | 5 |
| &emsp; - Pouring cereal into the container | 300 | 1 |
| Total (excluding bonus rewards) | 1490 |
| **Bonus Rewards** |
| &emsp; - Picking up an object from the shopping bag | 50 | 5 |
| &emsp; - Picking up a tiny object | 70 | 1 |
| &emsp; - Placing a tiny object | 30 | 1 |
| &emsp; - Picking up a heavy object | 70 | 1 |
| &emsp; - Placing a heavy object | 30 | 1 |
| Total (bonus rewards only) | 450 |
| **Deus Ex Machina Penalties** |
| &emsp; - Perceiving object and categorizing it wrongly | -15 | 10 |
| &emsp; - A human handing an object over to the robot | -50 | 5 |
| &emsp; - A human placing an object in the cabinet | -15 | 5 |
| &emsp; - A human placing an object in the cabinet next to similar objects | -50 | 5 |
| &emsp; - A human pointing at a target location | -25 | 5 |
| &emsp; - A human opening the first cabinet door | -200 | 1 |
| &emsp; - A human opening the second cabinet door | -100 | 1 |
| &emsp; - Spilling cereal while pouring | -100 | 1 |
| &emsp; - Leaving cereal in the box | -100 | 1 |
| &emsp; - A human pouring cereal in the bowl | -300 | 1 |
| **Deus Ex Machina Penalties** |
| &emsp; - Perceiving object and categorizing it wrongly | -15 | 10 |
| &emsp; - A human handing an object over to the robot | -50 | 5 |
| &emsp; - A human placing an object in the cabinet | -15 | 5 |
| &emsp; - A human placing an object in the cabinet next to similar objects | -50 | 5 |
| &emsp; - A human pointing at a target location | -25 | 5 |
| &emsp; - A human opening the first cabinet door | -200 | 1 |
| &emsp; - A human opening the second cabinet door | -100 | 1 |
| &emsp; - Spilling cereal while pouring | -100 | 1 |
| &emsp; - Leaving cereal in the box | -100 | 1 |
| &emsp; - A human pouring cereal in the bowl | -300 | 1 |
| Total (including bonus rewards) | 1940 |
<!-- | &emsp; - Opening the first cabinet door | 200 | 1 | -->
<!-- | &emsp; - Opening the second cabinet door | 100 | 1 | -->
<!-- | &emsp; - Autonomously Picking any Object | 50 | N/A | -->
<!-- | &emsp; - Autonomously Placing any Object | 50 | N/A | -->

**Score sheet for scorers**: [(TBD) SG-score_sheet]()
<!-- **Score sheet for scorers**: [SG-score_sheet](./doc/iHR-SG-score_sheet.pdf) -->


## Instructions

### To OC/TC

On Setup Day:
* Announce which table and cabinet will be used.
* Announce a rough location for the table.
* Select which bags will be used.
* Select which container will be used.

Before the competition starts:
* Place 5–10 objects on the table.
* Place the container and cornflakes on the table.
* Place 5–10 objects in a bag near the table.
* Place objects in the cabinet, grouping them by category or similarity.
* Close the cabinet doors.

### To Volunteer

Volunteers are not involved in this task.
