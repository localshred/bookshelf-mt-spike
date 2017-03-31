# Bookshelf.js + Express spike

Just learning how to get MT to work with [Bookshelf.js](http://bookshelfjs.org/) and Express.

## tl;dr

Knex integration is nice (esp with migrations), model definition is nice, but queries are just plain weird especially regarding relations. Feels like half an ORM where plugins are meant to solve the other half.

## Notes

1. No validation lib built-in, need to use something like Joi or validate.js.
2. No attribute definitions on model, it uses the connection to determine attrs (like AR).
3. Seems infeasible without bookshelf-modelbase (better static functions, validation support w/ Joi).
4. Defining associations are easier using the registry plugin (avoids cyclic dependencies).
5. Querying associations is more esoteric (you have to call related('otherModel').fetch({...}))

* "destroyed" event doesn't actually provide which model was deleted (not even an id). "destroying" event does but you have no way of knowing that operation succeeded... Mind Boggling.

## Other spikes

+ [knex](https://github.com/localshred/knex-mt-spike)
+ [Sequelize](https://github.com/localshred/sequelize-mt-spike)
+ [TypeORM](https://github.com/localshred/typeorm-mt-spike)
