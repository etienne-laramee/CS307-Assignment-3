# Component & User Interface Design
## The purpose and uses of class-based component design
The purpose of class-based component design is to make it easier to organize a complex application by abstracting and modularizing concepts into a set of common data and functionalities. By aggregating these, we create classes that represent the way a real object interacts. It is useful also to make classes modular and separate their concerns so that they can be more easily swapped or moved around, making more of the software code reusable.

Class-based component design is commonly used in web application development and video game development. For example, in a web app, a button class is a recurring object that benefits a lot from being made into a reusable class. By creating children from this parent class, developers can easily create new buttons with the same style but with slightly different behaviors elsewhere in the application. In video game development, a character class is useful as a reusable component, especially when there is a need to create multiple friends or enemies with similar but slightly different attributes and behaviors.
## A testing plan for ThermoSmart's software
Testing for this system will be done at different levels. First and most granular, unit testing. Then integration testing to test the interaction of multiple components together. Then system testing to validate the whole system is working properly. And finally, user acceptance testing to simulate real-world operations.
### 1. Unit testing:

Each component should be tested individually by simulating input and validating the output.

Individual components should consist of:
- Thermostat hardware/firmware
- Control Unit
    - API endpoints
    - Database queries
    - Appliance control
- Mobile App
- Web App
- Web Server API endpoints

### 2. Integration testing
For testing the interaction of multiple components, testing should be done between all the components, for example: From thermostat to control unit. Then from control unit to database and so on. This ensures communication between components works and that input and output is valid.
### 3. System testing
At this point everything is put together. Testing is done first for "Happy Flow" or the typical expected usage. Some more extensive tests should also be done to cover edge cases.
### 4. User acceptance testing
We should have a working system now. But we have not exhaustively tested it, as it is not realistic to think of each and every combination of configuration and input. This is where we get help from people outside ThermoSmart's development team. The input from "real" users is useful because they don't use the system the same way as those who developed it. With these kinds of tests we cover more edge cases that we haven't thought of before.

### Pre-launch gaps in the testing plan
There are so many real-world factors that cannot be extensively tested, such as:
- Client side devices like their wifi router and mobile devices
- Physical factors like house layout, extreme climate and weather
- Number of people using the system at the same time.
## ThermoSmart UI design justifications
The UI of the thermostats is designed to be very simple and display only the minimum information to perform their required tasks while being intuitive for the user. The information displayed is limited to the current ambient temperature at the center of the circle. Over or under is a colored bar indicating the desired temperature, if it varies from the ambient temperature. On the right is a throttle wheel style scroll bar for adjusting the desired temperature.

The UI for the mobile/web app is also simple. The main screen is a grid that contains an icon for each thermostat representing a named room.

When selecting one of the rooms, the screen presented is split in two, the upper half is a mini version of the thermostat, displaying the ambient temperature and the desired room temperature. At the bottom is a tabbed list of the configured hours and their desired temperature.

The day tabs show in a bright color the selected day and the schedule items below display what is the desired temperature that should start at the specified time. An "x" button for each entry makes it easy to remove a configured time and the button "+" at the bottom makes it quick to add a new one.

The featured UI mockups do not represent a finished product. Their intent is to visualize the information displayed and the potential operation flow.

## UI Testing plan
A testing plan for the thermostats and the mobile/web app would incorporate the following steps:
### 1. Components testing
Each component is tested individually. For example, the slider on the thermostat should correctly modify the desired temperature. The "+" button on the mobile app should correctly add a new editable schedule row.
### 2. Responsive display testing
The web and mobile applications should be tested for a variety of screen dimensions. At least the following should be supported, mobile phone, tablet and wide screen on PC.
### 3. Accessibility testing
Navigation should be intuitive and easy. Colors and contrast should satisfy visually impaired and color-blind people. Screen readers should be able to pick up on relevant labels.
### 4. Usability testing
Finally, non-technical users should have zero problem using the apps and thermostats. The functionalities should be intuitive and easy to use.
## Bibliography
Gloag, D. (2022, September 22) Class-Based Component Design: Principles & Process. Study.com. <https://study.com/academy/lesson/class-based-component-design-principles-process.html>

TechTarget. (n.d.). User interface (UI). TechTarget. <https://whatis.techtarget.com/definition/user-interface-UI>

Facebook, Inc. (n.d.). React documentation: Component. React.dev. <https://react.dev/reference/react/Component#component>

Chandran, S. (2025). Game development: Implementing OOP concepts in a 2D game.
LinkedIn.com. <https://www.linkedin.com/pulse/game-development-implementing-oop-concepts-2d-suchithra-chandran-flrec/>