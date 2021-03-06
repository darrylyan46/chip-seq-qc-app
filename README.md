# ChIP-DB
A MEAN (**M**ongoDB, **E**xpressJS, **A**ngular2, **N**odeJS) web application that visualizes
and displays ChIP-seq QC metrics for assessing and validating sample quality for
[the Reddy Lab](http://reddylab.org/). You can either view the deployed web application [here](http://67.159.92.22:4200/)
or create a local version through the instructions below.

## Getting Started

Clone the project repository to your local device. You will need to download and setup
[MongoDB](https://www.mongodb.com/download-center?jmp=tutorials#enterprise).

#### Database initialization
Once you have MongoDB setup on your local device, you will need to import data. To import the data provided in the
project directory, use the following code from your shell:

```
mongoimport -d chipseq_qc -c samples --type tsv --file <Your-Project-Repo>/chipseq_QCsummary.tsv --headerline
```

This will initialize your database with the appropriate collections. You will need to run `mongod` from your shell before running the app in order to host the database on your local device. 

#### Running the app
First, run `npm install` in the project directory to install the appropriate dependencies. Then, run `npm start` (or `nodemon` if you have it) for the Express/NodeJS server. Then in a separate tab, navigate to the *angular-src* directory and run `npm install`. Once finished, run `ng serve` from the *angular-src* directory in order to run the dev server for Angular2. Navigate to `http://localhost:4200/` to use.

## Built With
* [MongoDB](https://www.mongodb.com/) - A document-oriented NoSQL database
* [ExpressJS](https://expressjs.com/) - A minimal web-application framework for Node.js
* [Angular](https://angular.io/) - A front-end Typescript framework for dynamic web apps.
* [Node.js](https://nodejs.org/en/) - A Javascript runtime.
* [plotFingerprint](http://deeptools.readthedocs.io/en/latest/content/tools/plotFingerprint.html) - A Python tool
created by [deepTools](http://deeptools.readthedocs.io/en/latest/index.html) for analysis of ChIP-seq data.
* [Docker](https://www.docker.com/) - A software container platform that makes shipping and using software easier by containerizing system libraries and dependencies.

## Author
Darryl Yan
