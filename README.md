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
