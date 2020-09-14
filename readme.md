I GEAR GEEK: Coin Locker (コインロッカー)
===

:warning: Please follow these conditions before code!
- Coin Locker has only 1 locker and 12 units. 
There are 3 sizes : `S (#1, #4, #7, #10), M (#2, #5, #8, #11) and L (#3, #6, #9, #12)`.

    *This is a simulation of coin locker (Ex. Size of `#1` is `S` and size of `#12` is `L`)*

    |S|M|L|
    |-|-|-|
    |:one:|:two:|:three:|
    |:four:|:five:|:six:|
    |:seven:|:eight:|:nine:|
    |:one::zero:|:one::one:|:one::two:|
    
- The charge of locker usage (Based on unit size).
    
    | |:clock1: first 60 minutes| :clock2: next minutes|
    |-|-|-|
    |S|50 THB|25 THB|
    |M|100 THB|50 THB|
    |L|200 THB|100 THB|

- The user can insert coin: `1 THB, 2 THB, 5 THB, and 10 THB`
- The user can insert bill: `20 THB, 50 THB, 100 THB, 500 THB and 1000 THB`
- Can't select the same locker with other users in `Realtime`. (`User A` select unit of `#1` on another page then `User B` will see a unit of `#1`, that is not available to select without refresh page.)
- :+1: Design User Interface (UI) of coin locker based on good user experience (UX). 
- :+1: Focus on good [code quality](https://medium.com/@mkt_43322/why-is-code-quality-such-a-big-deal-for-developers-91bdace85d44).
  - Readability, consistency — how easy it is to read and understand sections of the code; this includes code clarity, simplicity, and documentation.
  - Predictability, reliability, and robustness — software behavior should be predictable, and not prone to hidden bugs.
  - Maintainability and extensibility — fixing, updating and improving software should be as simple as possible, not inherently complex.
- Technologies
  - Frontend : Vue or Nuxt.js
  - CSS Framework : Bootstrap or Vuetify
  - Backend (RESTful API or [GraphQL](https://graphql.org/)) : AdonisJS or Node.js
  - Database : mariaDB or MongoDB (We recommend [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
- Bonus!!
    - Unit and Integration testing such as
        - [phpunit](https://phpunit.de/)
        - [jest](https://jestjs.io/)
    - UI testing with automate testing tools such as
       - [cypress](https://www.cypress.io/)
       - [Robot Framework](https://robotframework.org/)
       - [katalon](https://www.katalon.com/)
    
- Scoring criteria

    |Task|Must have|Score|
    |-|-|-|
    |Frontend|:white_check_mark:|35|
    |Backend|:white_check_mark:|35|
    |Database|:white_check_mark:|10|
    |Deployment|:white_check_mark:|10|
    |Bonus|:white_large_square:|10|


**Test cases**  

|   | Story | Unit selected | Can select? | Duration of deposit (Minutes) | Insert | Charge | Change | Got item back? |
|---|-------|------------------|------------|------------|-----------|----------|------------|------------|
| 1 |User select unit of `#1` and insert 1,000 baht for charge |1|true|60|1000|50|500 x 1, 100 x 4, 50 x 1|true
| 2 |User select unit of `#1` and insert 100 baht for charge |1|true|61|100|75|20 x 1, 5 x 1|true
| 3 |User select unit of `#2` and insert 100 baht for charge |2|true|120|100|150|100 x 1|false
| 4 |User select unit of `#2` but this unit has been used by another user |2|false|-|-|-|-|-
| 5 |User select unit of `#12` and insert 400 baht for charge|12|true|145|400|400|0|true

:ok_hand: Acceptance agreement
---

1. Fork this GitHub project.
2. Open `issue` feature in your repository (Options > Features > Checked on Issues) [#Reference](https://softwareengineering.stackexchange.com/questions/179468/forking-a-repo-on-github-but-allowing-new-issues-on-the-fork)
3. Put your code in the `exercise` folder.
4. Publish your project on hosting, cloud or something that we can play it :) (We recommend  DigitalOcean, Firebase Hosting or Heroku)

Any question? :see_no_evil::hear_no_evil::speak_no_evil:
---
Open your issue from this link below

https://github.com/igeargeek/fullstackdev-fulltime-challenge/issues
