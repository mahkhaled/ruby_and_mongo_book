ruby_and_mongo_book
===================

* Map reduce
* Don't forget embedded_in because it will cause a lot of problems
* SCI Single Collection Inheritance vs Basic Polymorphic Relation (delegates)

Ch6
===

* Background index to avoid blocking operations
* Geospatial index
* Dynamic fields, you won't have getter and setter. However can access using [] ex: book[:title] = "sss"
* Localizatino fields
field :price, localize: true
* inverse_of between two associations will update the other association when chaning one of them. Ex: followers & following relations
* include Mongoid::Paranoia, that is all.

Ch7 Performance
===============

* db.setProfilingLevel(1) => 0: disabled, 1: slow more than 100ms, 2: all
* if nscanned is much higher than nreturned, then you need to add an index
* Explain function `db.authors.find({name: /in/}).explain()`
* covered index doesn't search the document however only search the index so exclude _id ex:`db.authors.find({name: /in/}, {_id:0, name: 1}).explain()`
* Don't index table with many inserts/updates.
