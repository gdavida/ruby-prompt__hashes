---
title: Hashes
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is a Hash?

-a hash is similar to an array, a hash is a colection of PAIRS of information
    -each pair is made of a name and a value
( https://www.codecademy.com/forum_questions/52a69117282ae3085d000d63 )

    aka:
    -associative array
    -dictionary
    -HashMap
    ( https://rubymonk.com/learning/books/1-ruby-primer/chapters/10-hashes-in-ruby/lessons/46-introduction-to-ruby-hashes )
    

# What are some examples of information that would be Hashes as opposed to some other data type?

When you want to reference whatever collection of data by something more specific than just an order.
    my_pets = {'girl_dog' => 'Clementine', 'boy_dog' => 'Henry', 'cat' => 'Bathtub'}
    puts my_pets['boy_dog']  #==> Henry
    
Or if you have the same set of information you need to collect multiple times
    davida = {'street_number' => '230', 'street_name' => 'Minnesota Avenue', 'city' => 'Sioux Falls', 'state' => 'SD'}
    patty = {'street_number' => '908', 'street_name' => 'South 4th Street', 'city' => 'Norfolk', 'state' => 'NE'}
    
# How are Hashes and Arrays similar? How are they different?

BOTH
-collections of data
-used to store and retrieve

ARRAYS
-index by automatic number order
-add by push or <<

HASHES
-indexed by assigned key
-can be easier to maintain and manipulate, because you can remember words for indices better than a number
-hash_name['key'] = 'value'

# How do you retrieve a particular value from a Hash?

davida = {'street_number' => '230', 'street_name' => 'Minnesota Avenue', 'city' => 'Sioux Falls', 'state' => 'SD'}

patty = {'street_number' => '908', 'street_name' => 'South 4th Street', 'city' => 'Norfolk', 'state' => 'NE'}

puts davida['city'] + ', ' + patty['city']   #==>  Sioux Falls, Norfolk
    
# How do you add information to a Hash?
hash_name['key'] = 'value'
davida['zipcode'] = "57104" 

# How would you perform an operation on every element inside a Hash?

-each-pair (only use each when you want to convert each key-value pair into an array)
-each
array.each {|key, value| puts "#{key} occured #{value} times" }

# How would you change the value of a particular element in a Hash?

davida = {'street_number' => '230', 'street_name' => 'Minnesota Avenue', 'city' => 'Sioux Falls', 'state' => 'SD'}
davida{'city'} = "Pierre"
puts davida
  #=> {'street_number' => '230', 'street_name' => 'Minnesota Avenue', 'city' => 'Pierre', 'state' => 'SD'}

# How do you delete an element from a Hash?
cars = {"Ford" => "Aerostar","BMW" => "733i", "Mazda" => "MX6", "Chrysler" => "PT Cruiser", "Pontiac" => "Aztek"}
cars.delete("Ford")   #=> Aerostar
puts cars 
  #=> {"BMW" => "733i", "Mazda" => "MX6", "Chrysler" => "PT Cruiser", "Pontiac" => "Aztek"}

# What happens if you try to retrieve an element from a Hash that does not exist in the Hash?

drinks = { "coffee" => 2, "tea" => 2, "water" => 1}
drink["water"] = 3

puts drinks 
#=> { "coffee" => 2, "tea" => 2, "water" => 3}

# How do you determine how many elements are in a Hash?

same as everything else, with .length
drinks.length #=> 3