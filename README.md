Meet App
    Objective:
        To build a serverless, progressive web application (PWA) with React using a test-driven 
        development (TDD) technique. The application uses the Google Calendar API to fetch 
        upcoming events.  

    Feature 1: Filter Events by City

        Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.
        given: user hasn’t searched for any city
        when: the user opens the app
        then: the user should see a list of all upcoming events

        Scenario 2: User should see a list of suggestions when they search for a city.
        given: the main page is open
        when: user starts typing in the city textbox
        then: the user should see a list of cities (suggestions) that match what they’ve typed

        Scenario 3: User can select a city from the suggested list.
        given: the user was typing “Berlin” in the city textbox. And the list of suggested cities is showing
        when: the user selects a city from the list
        then: their city should be changed to that city and the user should receive a list of upcoming events in that city


    Feature 2: Show/hide an event's details

        Scenario 1: An event element is collapsed by default
            given: user is on main page
            when: events are displayed
            then: event element is collapsed by default
        Scenario 2: User can expand an event to see its details
            given: user has list of events
            when: user clicks on event details
            then: expands event details
        Scenario 3: User can collapse an event to hide its details
            given:  user is on event details
            when: user clicks on event details
            then: collapses event details

    Feature 3: Specify number of events

        Scenario 1: When user hasn’t specified a number, 32 is the default number
            given: user is searching for events
            when: no number of events entered
            then: automatically display 32 events
        Scenario 2: User can change the number of events they want to see
            given:  user is searching for events on main page
            when: user enters number of events
            then: user changes number of events displayed

    Feature 4: Use the app when offline

        Scenario 1: Show cached data when there’s no internet connection
            given: user opens app
            when: user has no internet connected
            then: show a cached data
        Scenario 2: Show error when user changes the settings (city, time range)
            given: user is offline
            when: user changes settings
            then: user recieves error message

    Feature 5: Data visualization

        Scenario 1: Show a chart with the number of upcoming events in each city
            given: user is on main page
            when: user enters location of events
            then: user recieves upcoming events number chart

