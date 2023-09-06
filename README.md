# js_calendarView - Calendar Extension
Renders the days of the selected calendar months as consecutive lines. Includes transition methods and calendar extensions.
Calendar Extension is a JavaScript library that allows you to easily integrate a customizable calendar component into your web application. It provides features for rendering and navigating through calendar months.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contents](#contents)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Features

- Display a calendar with customizable styling.
- Navigate between months using previous and next buttons.
- Extend calendar to past or future.
- Update the calendar view based on date input.
- Get and set 'GET' params of first and last month in sequence.
- Easily integrate the calendar into your web application.

## Installation
- Just download and place files in the root of the site.

## Usage
- Attach included js libraries.
- Create containers for calendar and navigation with different id's.
- Define an instance of DayFlow with id of calendar container.
- Get navigation buttons CalTemplate.navButtons([endMonth]) with param [endMonth] of DayFlow instance;
- Append navigation buttons to container.
- Run!

## Contents
- `dayflow.js` DayFlow.class : provide a comprehensive solution for managing and rendering calendar data, as well as handling user interactions for navigating the calendar. The code is well-organized and includes error handling for cases like selecting a non-existent calendar container or dealing with invalid date ranges.
- `shortdate.js` ShortDate.class : provides a human-readable simplified date object containing a bunch of convenience methods for manipulating dates. Created primarily to solve the problem of a zero date index.
- `shortdate.js` DateUtils.class : provides functionality to manipulate URL params, and contains month color definitions.
- `caltemplate.js` CalTemplate.class : contains various static methods for generating and manipulating calendar templates. You have to modify or replace all this template to customize your application.
- `index.html` : contains base style definition and demo code.

## Examples
...
`<body>
    <div id="calendar_nav">
    </div>
    <br>
    <div id="calendar_body">
    </div>
    <br>
    <div id="calendar_nav_down">
    </div>
    <script>
        // Define an instance of DayFlow object
        const DF = new DayFlow('#calendar_body');
        // Define and place navigation buttons on the top of the page
        const navbutts = CalTemplate.navButtons(DF.endMonth.getShortDate());
        document.querySelector('#calendar_nav').appendChild(navbutts);
        // Define and place navigation buttons on the bottom of the page 
        // Second param as TRUE allows to scroll page down when click
        const navbutts2 = CalTemplate.navButtons(DF.startMonth.getShortDate(), true);
        document.querySelector('#calendar_nav_down').appendChild(navbutts2);
        </script>
</body>`
...

## Contributing
- Developed by `Teftele` - https://github.com/Vsemhoy/
- You can use and modify this code as you want


## License
This project is licensed under the GNU Public License (GPL V3);
