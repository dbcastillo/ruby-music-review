# Code Challenge Review - Music

For this assignment, we'll be working with music connection! 

We have three models: `Musician`, `Fan`, and `Concert`.

For our purposes, a `Musician` has many `Fans`, a `Fan` has many `Musician`s, and a `Concert` belongs to a `Fan` and to a `Musician`.

`Musician` - `Fan` is a many to many relationship.

## Instructions

To get started, run `bundle install` while inside of this directory.

We've provided you with a tool that you can use to test your code. To use it, run `ruby tools/console.rb` from the command line. 

## Deliverables

Deliverables use the notation `#` for instance methods, and `.` for class methods.

### Musician

- `Musician#initialize`
  - Musician should be initialized with a name as string
- `Musician#genre`
  - Musician should be initialized with a genre as a string
- `Musician#instrument`
  - Musician should be initialized with a instrument as a string
- `Musician#concerts`
  - returns an array of all concerts for that Musician
- `Musician#add_concert(fan, day)`
  - given a **fan object** and day (as a string), create a new concert and associate it with that Musician and fan
- `Musician.genre_musician(genre)`
  - takes an argument of a genre and returns the first musician in this genre

### Fan
- `Fan#initialize`
  - Fan should be initialized with a name as string
- `Fan#musician`
  - returns a **unique** list of all musicians who this fan is connected to
- `Fan.all`
  - returns **all** of the Fan instances

### Concert
- `Concert#initialize`
  - Concert should be initialized with a musician object, fan object, and day (a string)
- `Concert#musician`
  - returns the musician object for that Concert
  - once a Concert is made, should not be able to change the musician
- `Concert.saturday`
  - returns the concerts made on a Saturday
