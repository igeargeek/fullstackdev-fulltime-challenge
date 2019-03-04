I GEAR GEEK : Coin Locker (コインロッカー)
===

Please follow these conditions before code!
- Coin Locker has only 1 locker and 12 units. 
There are 3 sizes : `S (#1, #4, #7, #10), M (#2, #5, #8, #11) and L (#3, #6, #9, #12).`

    *This is a simmulation of coin locker (Ex. Unit of #1 is `S` size)*

    |S|M|L|
    |-|-|-|
    |1|2|3|
    |4|5|6|
    |7|8|9|
    |10|11|12|
    
- Charge of locker usage (Based on unit size).
    
    | |first 60 minutes|next minutes|
    |-|-|-|
    |S|50 THB|25 THB|
    |M|100 THB|50 THB|
    |L|200 THB|100 THB|

- User can insert coin : `1 THB, 2 THB, 5 THB and 10 THB`, insert bill : `20 THB, 50 THB, 100 THB, 500 THB and 1000 THB`
- Design User Interface (UI) of coin locker based on good user experience (UX). 
- Focus on good [code quality](https://medium.com/@mkt_43322/why-is-code-quality-such-a-big-deal-for-developers-91bdace85d44).
  - Readability, consistency — how easy it is to read and understand sections of the code; this includes code clarity, simplicity, and documentation.
  - Predictability, reliability, and robustness — software behavior should be predictable, and not prone to hidden bugs.
  - Maintainability and extensibility — fixing, updating and improving software should be as simple as possible, not inherently complex.
- Technologies
    - CSS Framework : Bootstrap
  - Frontend : React, Vue
  - API (RESTful API or [GraphQL](https://graphql.org/)) : Laravel (PHP) or Node.js
  - Database : MongoDB (We recommend [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
- Bonus point
    - Unit and Integration testing such as
        - [phpunit](https://phpunit.de/)
        - [jest](https://jestjs.io/)
  - UI testing with automate testing tools such as
    - [cypress](https://www.cypress.io/)
    - [Robot Framework](https://robotframework.org/)
    - [katalon](https://www.katalon.com/)


**Test cases**  

|   | Story | Unit selected | Can select? | Duration of deposit (Minutes) | Insert | Charge | Change | Got item back? |
|---|-------|------------------|------------|------------|-----------|----------|------------|------------|
| 1 |User select unit of #1 and insert 1,000 baht for charge |1|true|60|1000|50|500 x 1, 100 x 4, 50 x 1|true
| 2 |User select unit of #1 and insert 100 baht for charge |1|true|61|100|75|20 x 1, 5 x 1|true
| 3 |User select unit of #2 and insert 100 baht for charge |2|true|120|100|150|100 x 1|false
| 4 |User select unit of #2 but this unit has been used by another user |2|false|-|-|-|-|-
| 5 |User select unit of #12 and insert 400 baht for charge|12|true|145|400|400|0|true

Acceptance agreement
---

1. Fork this github project.
2. Open `issue` feature in your repository (Options > Features > Checked on Issues) [#Reference](https://softwareengineering.stackexchange.com/questions/179468/forking-a-repo-on-github-but-allowing-new-issues-on-the-fork)
3. Put your code in `exercise` folder.
4. Publish your project on hosting, cloud or something that we can play it :) (We recommend  DigitalOcean, Firebase Hosting or Heroku)

Any question?
---
Open your issue from this link below

https://github.com/igeargeek/fullstackdev-fulltime-challenge/issues
