# All the News That's Fit to Scrape

## Overview

In this assignment, you'll create a web app that lets users view and leave comments on the latest news. But you're not going to actually write any articles; instead, you'll flex your Mongoose and Cheerio muscles to scrape news from another site.


**NOTES:**
* If you want to earn complete credit for your work, you must use all five of these packages in your assignment.

* In order to deploy the project to Heroku, you must set up an mLab provision. mLab is remote MongoDB database that Heroku supports natively. Follow these steps to get it running:
- Create a Heroku app in your project directory.
- Run this command in your Terminal/Bash window:

`heroku addons:create mongolab`

- This command will add the free mLab provision to your project.
* When you go to connect your mongo database to mongoose, do so the following way:

```js
// If deployed, use the deployed database. Otherwise use the local mongoHeadlines database
var MONGODB_URI = process.env.MONGODB_URI || "mongodb://localhost/mongoHeadlines";

mongoose.connect(MONGODB_URI);
```

* This code should connect mongoose to your remote mongolab database if deployed, but otherwise will connect to the local mongoHeadlines database on your computer.

## Instructions

* Create an app that accomplishes the following:

1. Whenever a user visits your site, the app should scrape stories from a news outlet of your choice and display them for the user. Each scraped article should be saved to your application database. At a minimum, the app should scrape and display the following information for each article:

* Headline - the title of the article

* Summary - a short summary of the article

* URL - the url to the original article

* Feel free to add more content to your database (photos, bylines, and so on).

2. Users should also be able to leave comments on the articles displayed and revisit them later. The comments should be saved to the database as well and associated with their articles. Users should also be able to delete comments left on articles. All stored comments should be visible to every user.

* Beyond these requirements, be creative and have fun with this!

### Helpful Links

* [MongoDB Documentation](https://docs.mongodb.com/manual/)
* [Mongoose Documentation](http://mongoosejs.com/docs/api.html)
* [Cheerio Documentation](https://github.com/cheeriojs/cheerio)


---
<sub> &copy; Paul Xu at UofT Coding Boot Camp June 2019 </sub>


