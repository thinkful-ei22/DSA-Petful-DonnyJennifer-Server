#Petful Api

##Data Structure:

Cats and dogs are stored in queues.

##Getting:

A GET request will peek into the queue and return the first animal in the queue.

**Sample request:**

app.get('/api/cat', (req,res) => {
  res.json(catQueue.peek());
});

**Sample response (animal peeked):**
`{
    "imageURL": "https://assets3.thrillist.com/v1/image/2622128/size/tmg-slideshow_l.jpg",
    "imageDescription": "Orange bengal cat with black stripes lounging on concrete.",
    "name": "Fluffy",
    "sex": "Female",
    "age": 2,
    "breed": "Bengal",
    "story": "Thrown on the street"
}`

##Deleting:

When a user clicks "Adopt!" a DELETE request is sent.  The DELETE request dequeues the first animal from the queue.

**Sample request:**

`app.delete('/api/cat', (req,res) => {
  res.json(catQueue.dequeue());
});`

**Sample response (animal deleted):**
`{
    "imageURL": "https://assets3.thrillist.com/v1/image/2622128/size/tmg-slideshow_l.jpg",
    "imageDescription": "Orange bengal cat with black stripes lounging on concrete.",
    "name": "Fluffy",
    "sex": "Female",
    "age": 2,
    "breed": "Bengal",
    "story": "Thrown on the street"
}`

**Target Audience:** Animal Lovers
**MVP features:** adopt a cat or adopt a dog
**Tech Stack:** Express and Node on the backend, React/Redux on the frontend.
**Future plans:** allow users to add animals, allow users to choose which breed displays, put data in a database.