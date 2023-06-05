function numTest(number) {
  return new Promise(function(resolve, reject) {
    if (number > 20) {
      resolve(number + " is greater than 20");
    } else {
      reject(number + " is not greater than 20");
    }
  });
}

// Example usage:
numTest(15)
  .then(function(result) {
    console.log(result);
  })
  .catch(function(error) {
    console.log(error);
  });


function bookFlight() {
  return new Promise(function(resolve, reject) {
    // Simulating asynchronous operation
    setTimeout(function() {
      resolve("Flight booked");
    }, 2000);
  });
}

function bookHotel() {
  return new Promise(function(resolve, reject) {
    // Simulating asynchronous operation
    setTimeout(function() {
      resolve("Hotel booked");
    }, 1000);
  });
}

bookFlight()
  .then(function(flightResult) {
    console.log(flightResult);
    return bookHotel();
  })
  .then(function(hotelResult) {
    console.log(hotelResult);
  })
  .catch(function(error) {
    console.log(error);
  });


function add(a, b) {
  return new Promise(function(resolve, reject) {
    setTimeout(function() {
      resolve(a + b);
    }, 1000);
  });
}

function subtract(a, b) {
  return new Promise(function(resolve, reject) {
    setTimeout(function() {
      resolve(a - b);
    }, 1000);
  });
}

function multiply(a, b) {
  return new Promise(function(resolve, reject) {
    setTimeout(function() {
      resolve(a * b);
    }, 1000);
  });
}

async function performOperations() {
  try {
    var result1 = await add(10, 5);
    console.log("Addition result: " + result1);

    var result2 = await subtract(result1, 3);
    console.log("Subtraction result: " + result2);

    var result3 = await multiply(result2, 4);
    console.log("Multiplication result: " + result3);
  } catch (error) {
    console.log(error);
  }
}

performOperations();

