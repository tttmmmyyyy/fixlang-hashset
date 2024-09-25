# `module HashSet`

# Types and aliases

## `namespace HashSet`

### `type HashSet k = unbox struct { ...fields... }`

#### field `_hashmap : HashMap::HashMap k ()`

# Traits and aliases

# Trait implementations

# Values

## `namespace HashSet`

### `contains : [k : Hash::HashKey] k -> HashSet::HashSet k -> Std::Bool`

Checks whether a hashset contains an element.

### `empty : Std::I64 -> HashSet::HashSet k`

Creates an empty HashSet which is reserved so that it will not rehash until size exceeds the spacified value.

### `erase : [k : Hash::HashKey] k -> HashSet::HashSet k -> HashSet::HashSet k`

Erases an element from a HashSet.

### `from_iter : [k : Hash::HashKey] Std::Iterator k -> HashSet::HashSet k`

Constructs a HashSet from an iterator of elements.

### `get_capacity : HashSet::HashSet k -> Std::I64`

Gets capacity of a HashSet.

### `get_size : HashSet::HashSet k -> Std::I64`

Gets size (number of elements) of a HashSet.

### `insert : [k : Hash::HashKey] k -> HashSet::HashSet k -> HashSet::HashSet k`

Inserts an element into a HashSet.

### `intersect : [k : Hash::HashKey] HashSet::HashSet k -> HashSet::HashSet k -> HashSet::HashSet k`

Calculates intersection of two Hashsets.

### `merge : [k : Hash::HashKey] HashSet::HashSet k -> HashSet::HashSet k -> HashSet::HashSet k`

Calculates union of two HashSets.

### `reserve : [k : Hash::HashKey] Std::I64 -> HashSet::HashSet k -> HashSet::HashSet k`

Reserves a HashSet so that it will not rehash until size exceeds the spacified value.

### `to_iter : HashSet::HashSet k -> Std::Iterator k`

Converts a HashSet into an iterator.

## `namespace HashSet::HashSet`

### `@_hashmap : HashSet::HashSet k -> HashMap::HashMap k ()`

Retrieves the field `_hashmap` from a value of `HashSet`.

### `act__hashmap : [f : Std::Functor] (HashMap::HashMap k () -> f (HashMap::HashMap k ())) -> HashSet::HashSet k -> f (HashSet::HashSet k)`

Updates a value of `HashSet` by applying a functorial action to field `_hashmap`.

### `mod__hashmap : (HashMap::HashMap k () -> HashMap::HashMap k ()) -> HashSet::HashSet k -> HashSet::HashSet k`

Updates a value of `HashSet` by applying a function to field `_hashmap`.

### `set__hashmap : HashMap::HashMap k () -> HashSet::HashSet k -> HashSet::HashSet k`

Updates a value of `HashSet` by setting field `_hashmap` to a specified one.