# HashSet

Defined in hashset@1.1.2

## Values

### namespace HashSet

#### contains

Type: `[k : Hash::HashKey] k -> HashSet::HashSet k -> Std::Bool`

Checks whether a hashset contains an element.

##### Parameters

- `key` : The element to search for.
- `set` : The HashSet to search in.

#### empty

Type: `Std::I64 -> HashSet::HashSet k`

Creates an empty HashSet which is reserved so that it will not rehash until size exceeds the spacified value.

##### Parameters

- `capacity` : The initial capacity of the HashSet.

#### erase

Type: `[k : Hash::HashKey] k -> HashSet::HashSet k -> HashSet::HashSet k`

Erases an element from a HashSet.

##### Parameters

- `key` : The element to erase.
- `set` : The HashSet to erase from.

#### from_iter

Type: `[k : Hash::HashKey, it : Std::Iterator, Std::Iterator::Item it = k] it -> HashSet::HashSet k`

Constructs a HashSet from an iterator of elements.

##### Parameters

- `iter` : The iterator of elements.

#### get_capacity

Type: `HashSet::HashSet k -> Std::I64`

Gets capacity of a HashSet.

##### Parameters

- `set` : The HashSet to get capacity of.

#### get_size

Type: `HashSet::HashSet k -> Std::I64`

Gets size (number of elements) of a HashSet.

##### Parameters

- `set` : The HashSet to get size of.

#### insert

Type: `[k : Hash::HashKey] k -> HashSet::HashSet k -> HashSet::HashSet k`

Inserts an element into a HashSet.

##### Parameters

- `key` : The element to insert.
- `set` : The HashSet to insert into.

#### intersect

Type: `[k : Hash::HashKey] HashSet::HashSet k -> HashSet::HashSet k -> HashSet::HashSet k`

Calculates intersection of two Hashsets.

##### Parameters

- `fst` : The first HashSet.
- `snd` : The second HashSet.

#### merge

Type: `[k : Hash::HashKey] HashSet::HashSet k -> HashSet::HashSet k -> HashSet::HashSet k`

Calculates union of two HashSets.

##### Parameters

- `fst` : The first HashSet.
- `snd` : The second HashSet.

#### reserve

Type: `[k : Hash::HashKey] Std::I64 -> HashSet::HashSet k -> HashSet::HashSet k`

Reserves a HashSet so that it will not rehash until size exceeds the spacified value.

##### Parameters

- `capacity` : The capacity to reserve.
- `set` : The HashSet to reserve.

#### to_iter

Type: `HashSet::HashSet k -> HashSet::HashSetIterator k`

Converts a HashSet into an iterator.

##### Parameters

- `set` : The HashSet to convert to an iterator.

## Types and aliases

### namespace HashSet

#### HashSet

Defined as: `type HashSet k = unbox struct { ...fields... }`

##### field `_hashmap`

Type: `HashMap::HashMap k ()`

#### HashSetIterator

Defined as: `type HashSetIterator a = Std::Iterator::MapIterator (HashMap::HashMapIterator (a, ())) (a, ()) a`

## Traits and aliases

## Trait implementations