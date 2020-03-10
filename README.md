# Disney Villain API

In this two part exercise you are tasked with create a REST API for accessing Disney Villain data, complete with test suite.

## Part One

In the initial commit to this project, you have been provided with data for Disney villains. Your task is to implement an Express driven REST API that allows a user to retrieve this data. Your API should store its data in a database table and implement the routes defined below. Create a branch called `part-one-answer` to do this work in.

### Requests and Expected Respones

#### Get All

**GET** `http://localhost:1337/villains`

**Response**
```JSON
[{
  name: 'Captain Hook',
  movie: 'Peter Pan',
  slug: 'captain-hook',
},
... all other movies
]
```

#### Get By Slug (Should 404 when not found)

**GET** `http://localhost:1337/villains/jafar`

**Response**
```JSON
{
  name: 'Jafar',
  movie: 'Aladdin',
  slug: 'jafar',
}
```

#### Create New

**POST** `http://localhost:1337/villains`

**Body**
```JSON
{
  name: 'Red Skull',
  movie: 'Captain America: The First Avenger',
  slug: 'red-skull',
}
```

**Response**
```JSON
{
  id: 21,
  name: 'Red Skull',
  movie: 'Captain America: The First Avenger',
  slug: 'red-skull',
  updatedAt: '2020-04-24T13:12:15.656Z',
  createdAt: '2020-04-24T13:12:15.656Z'
}
```

## Part Two

In a branch called `part-two-answer`, continuing from your `part-one-answer` branch, you are tasked with creating a test suite for your API. You should have tests for each of your controller functions. These tests should cover both happy path as well as error cases.
