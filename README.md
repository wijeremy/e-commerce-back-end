 
# E-Commerce Back End
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[Visit the repository for this app.](https://github.com/wijeremy/e-commerce-back-end)

[View a walkthrough of me using the app.](https://www.youtube.com/watch?v=z_ye7mdJn6I&ab_channel=HermeticHippie)
## Description
I wanted to try using sequelize in a real world environment. This also helped me practice routing.
You can use this app to organize information on a site that sells products. When paired with a front end, one could add code that reduces stock when items are purchased. However, the code presented here simply allows a user to update information on the site manually through CRUD commands to the server.
I learned a lot about routing and using ORMs like sequelize. It gave me good practice with inter table relationships and forced me to better understand many to many table relationships. It also helped me understand the value of running a server on force: true. I began my project not wanting to use it because it was more cumbersome to initialize the app (having to seed after I spin up the server), but it was necessary to get certain elements of the app to work. Specifically, I could not delete categories -- a parent table -- without it.
## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contributing](#contributing)
- [Tests](#tests)
- [Questions](#questions)
## Installation
Run npm install. Open mysql in your terminal and run the schema.sql file. Run server.js in node. Then open a new terminal windo and run './seeds/index.js' from the root file in node. After that, you should be able to interact with the server using an program like Insomnia.
## Usage
Once your server is up and seeded, open a program like Insomnia that lets you CRUD to the server. There you can navigate to localhost:3001/api and use the routes /categories, /products, and /tags to GET the entire contents of those tables in the database. You can also search individual rows of those tables by putting / and the id of the row you would like to search for after the table names. Categories takes { "category_name": STRING } for its POST and PUTs requests. Products takes { "product_name": STRING, "price": DECIMAL, "stock": INT, "tagId": INT } for its POST and PUTs. Tag takes { "tag_name": STRING } for its POST and PUTs. Navigate to /{table name} to GET or POST. Navigate to /{table name}/{id} to PUT or DELETE.
## License
I am using [MIT](https://opensource.org/licenses/MIT) to license this app.
## Contributing
See license.
## Tests
No tests included.
## Questions?
Email me at jeremydavwilliams@gmail.com or visit [my github page](github.com/wijeremy)
  