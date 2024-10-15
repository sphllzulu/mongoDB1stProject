
# Codetribe MongoDB Project

This project involves using MongoDB to create a database called `Codetribe` and setting up collections for `Facilitators`, `Trainees`, and `Projects`. Below are the specific instructions and MongoDB shell commands to achieve the project outcomes.

## Prerequisites

- MongoDB should be installed on your system.
- The `mongosh` command-line tool should be set up and ready for use.
- A MongoDB server should be running locally or remotely to connect.

## Starting the MongoDB Shell (Mongosh)

To start the MongoDB shell (Mongosh) and connect to your local database instance, open your terminal or command prompt and run:

```bash
mongosh
```

If you're connecting to a remote MongoDB server, use the following command (replace `<connection-string>` with your server's connection string):

```bash
mongosh <connection-string>
```

Once inside the MongoDB shell, you can start executing the commands listed below to create the database and insert data.

## Step-by-Step Instructions

### 1. Create the Database

Create a new database named `Codetribe`:

```bash
use Codetribe
```

This will either switch to the `Codetribe` database if it already exists or create it if it doesn't.

### 2. Create Collections

Create the `Facilitators`, `Trainees`, and `Projects` collections.

```bash
db.createCollection('Facilitators')
db.createCollection('Trainees')
db.createCollection('Projects')
```

### 3. Insert Documents into Collections

#### Inserting a document into the `Facilitators` collection:

```bash
db.Facilitators.insertOne({
  Name: "John Doe",
  Location: "Johannesburg",
  Course: "Full Stack Development"
})
```

#### Inserting a document into the `Trainees` collection:

```bash
db.Trainees.insertOne({
  Name: "Jane Smith",
  Location: "Pretoria",
  Facilitator: "John Doe"
})
```

#### Inserting a document into the `Projects` collection:

```bash
db.Projects.insertOne({
  Name: "Hotel Booking System",
  Course: "Full Stack Development",
  Lesson: "Lesson 10"
})
```

### 4. Query the Collections

To view the inserted documents, you can query the collections like this:

#### Query all Facilitators:

```bash
db.Facilitators.find()
```

#### Query all Trainees:

```bash
db.Trainees.find()
```

#### Query all Projects:

```bash
db.Projects.find()
```

## Additional Commands

If you need to update a document or delete one, you can use the following commands:

#### Update a document in the `Facilitators` collection:

```bash
db.Facilitators.updateOne(
  { Name: "John Doe" },
  { $set: { Location: "Cape Town" } }
)
```

#### Delete a document from the `Trainees` collection:

```bash
db.Trainees.deleteOne({ Name: "Jane Smith" })
```

## Conclusion

This README outlines the necessary steps to create and manage the MongoDB database `Codetribe` and its collections. You can expand this project by adding more documents, querying data, or integrating MongoDB into an application using Node.js or another backend technology.
