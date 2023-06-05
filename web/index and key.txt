var student = {
  name: "David Rayy",
  sclass: "VI",
  rollno: 12
};

var values = Object.values(student);
console.log(values.join(", "));

function objectToList(obj) {
  return Object.entries(obj);
}

var student = {
  name: "David Rayy",
  sclass: "VI",
  rollno: 12
};

var pairs = objectToList(student);
console.log(pairs);


var mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(3);

console.log(mySet.has(2)); // Output: true

mySet.forEach(function(value) {
  console.log(value);
});



var myMap = new Map();
myMap.set("name", "John");
myMap.set("age", 25);
myMap.set("city", "London");

console.log(myMap.get("age")); // Output: 25

myMap.forEach(function(value, key) {
  console.log(key + " => " + value);
});


// Map example
var map = new Map();
map.set("a", 1);
map.set("b", 2);
map.set("c", 3);

map.delete("b");

console.log(map.size); // Output: 2

// Object example
var obj = {
  a: 1,
  b: 2,
  c: 3
};

delete obj.b;

console.log(Object.keys(obj).length); // Output: 2


// Set example
var set = new Set();
set.add(1);
set.add(2);
set.add(3);
set.add(2); // Duplicate value, ignored

console.log(set.size); // Output

