Create a function that transforms any positive number to a string representing the number in words. The function should work for all numbers between 0 and 999999.

Examples
number2words(0)  ==>  "zero"
number2words(1)  ==>  "one"
number2words(9)  ==>  "nine"
number2words(10)  ==>  "ten"
number2words(17)  ==>  "seventeen"
number2words(20)  ==>  "twenty"
number2words(21)  ==>  "twenty-one"
number2words(45)  ==>  "forty-five"
number2words(80)  ==>  "eighty"
number2words(99)  ==>  "ninety-nine"
number2words(100)  ==>  "one hundred"
number2words(301)  ==>  "three hundred one"
number2words(799)  ==>  "seven hundred ninety-nine"
number2words(800)  ==>  "eight hundred"
number2words(950)  ==>  "nine hundred fifty"
number2words(1000)  ==>  "one thousand"
number2words(1002)  ==>  "one thousand two"
number2words(3051)  ==>  "three thousand fifty-one"
number2words(7200)  ==>  "seven thousand two hundred"
number2words(7219)  ==>  "seven thousand two hundred nineteen"
number2words(8330)  ==>  "eight thousand three hundred thirty"
number2words(99999)  ==>  "ninety-nine thousand nine hundred ninety-nine"
number2words(888888)  ==>  "eight hundred eighty-eight thousand eight hundred eighty-eight"



function number2words(n){
  if (n === 0) {
    return "zero"
  }
  var nums = { 0: "zero", 1: "one", 2: "two", 3: "three", 4: "four", 5: "five", 6: "six", 7: "seven", 8: "eight", 9: "nine", 10: "ten", 11: "eleven", 12: "twelve", 13: "thirteen", 14: "fourteen", 15: "fifteen", 16: "sixteen", 17: "seventeen", 18: "eighteen", 19: "nineteen", 20: "twenty", 30: "thirty", 40: "forty", 50: "fifty", 60: "sixty", 70: "seventy", 80: "eighty", 90: "ninety", "000": "hundred", "0000": "thousand" }
  var strN = String(n)
  var final = ""
  for (var i = 0; i < strN.length; i++) {
    if (strN[i] === "0") {
      final += ""
    } else if (strN.length - i === 6) {
      final += nums[Number(strN[i])] + " " + nums["000"]
      if (Number(strN.substring(i+1, strN.length)) !== 0) {
        final += " "
      }
      if ((Number(strN[i+2]) === 0) && (Number(strN[i+1]) === 0)) {
        final += nums["0000"] + " "
      }
    } else if (strN.length - i === 5) {
      if (strN[i] === "1") {
          final += nums[Number(strN[i] + strN[i+1])] + " " + nums["0000"]
          if (Number(strN.substring(i+1, strN.length)) !== 0) {
            final += " "
          }
          i += 1
      } else { 
        final += nums[Number(strN[i] + "0")]
        if (Number(strN[i+1]) === 0) {
          final += " " + nums["0000"] + " "
        } else {
          final += "-"
        }
      }
    } else if (strN.length - i === 4) {
      final += nums[Number(strN[i])] + " " + nums["0000"]
      if (Number(strN.substring(i+1, strN.length)) !== 0) {
        final += " "
      }
    } else if (strN.length - i === 3) {
      final += nums[Number(strN[i])] + " " + nums["000"]
      if (Number(strN.substring(i+1, strN.length)) !== 0) {
        final += " "
      }
    } else if (strN.length - i === 2) {
        if (strN[i] === "1") {
          final += nums[Number(strN[i] + strN[i+1])]
          i += 1
        } else { 
          final += nums[Number(strN[i] + "0")]
          if (strN[i+1] != "0") {
            final += "-"
          }
        }
    } else if (strN.length - i === 1) {
      final += nums[Number(strN[i])]
    }
  }
  return final
}




Task:
Given an array arr of strings complete the function landPerimeter by calculating the total perimeter of all the islands. Each piece of land will be marked with 'X' while the water fields are represented as 'O'. Consider each tile being a perfect 1 x 1piece of land. Some examples for better visualization:

['XOOXO',
 'XOOXO',
 'OOOXO',
 'XXOXO',
 'OXOOO']
or 

 
should return: "Total land perimeter: 24", 
while


['XOOO',
 'XOXO',
 'XOXO',
 'OOXX',
 'OOOO']


should return: "Total land perimeter: 18"

Good luck!



function landPerimeter(arr) {
  var perimeter = 0
  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < arr[i].length; j++) {
      if (arr[i][j] === "X") {
        if (typeof (arr[i-1]) === "undefined") {
          perimeter += 1
        } else if (arr[i-1][j] === "O") {
          perimeter += 1
        } 
        if (typeof (arr[i+1]) === "undefined") {
          perimeter += 1
        } else if (arr[i+1][j] === "O") {
          perimeter += 1
        } 
        if (typeof (arr[i][j+1]) === "undefined") {
          perimeter += 1
        } else if (arr[i][j+1] === "O") {
          perimeter += 1
        } 
        if (typeof (arr[i][j-1]) === "undefined") {
          perimeter += 1
        } else if (arr[i][j-1] === "O") {
          perimeter += 1
        }
      }
    }
  }
  return "Total land perimeter: " + perimeter
}



A Man and his Umbrellas
Each morning a man walks to work, and each afternoon he walks back home.

If it is raining in the morning and he has an umbrella at home, he takes an umbrella for the journey so he doesn't get wet, and stores it at work. Likewise, if it is raining in the afternoon and he has an umbrella at work, he takes an umbrella for the journey home.

Given an array of the weather conditions, your task is to work out the minimum number of umbrellas he needs to start with in order that he never gets wet. He can start with some umbrellas at home and some at work, but the output is a single integer, the minimum total number.

The input is an array/list of consecutive half-day weather forecasts. So, e.g. the first value is the 1st day's morning weather and the second value is the 1st day's afternoon weather. The options are "clear", "sunny", "cloudy", "rainy", "windy" or "thunderstorms".

e.g. for three days, 6 values:

weather = ["rainy", "cloudy", "sunny", "sunny", "cloudy", "thunderstorms"]
N.B. He never takes an umbrella if it is not raining.

Examples:
minUmbrellas(["rainy", "clear", "rainy", "cloudy"])
// should return 2
// Because on the first morning, he needs an umbrella to take, and he leaves it at work.
// So on the second morning, he needs a second umbrella.

minUmbrellas(["sunny", "windy", "sunny", "clear"])
// should return 0
// Because it doesn't rain at all

minUmbrellas(["rainy", "rainy", "rainy", "rainy", "thunderstorms", "rainy"])
// should return 1
// Because he only needs 1 umbrella which he takes on every journey.


function minUmbrellas(weather) {
  var workUmb = 0
  var homeUmb = 0
  for (var i = 0; i < weather.length; i++) {
    if (i % 2 === 0 && (weather[i] === "rainy" || weather[i] === "thunderstorms")) {
      if (homeUmb === 0) {
        workUmb += 1
      } else if (homeUmb > 0 && (weather[i] === "rainy" || weather[i] === "thunderstorms")) {
        homeUmb -= 1
        workUmb += 1
      }
    } else if (i % 2 === 1 && (weather[i] === "rainy" || weather[i] === "thunderstorms")) {
      if (workUmb === 0) {
        homeUmb += 1
      } else if (workUmb > 0 && (weather[i] === "rainy" || weather[i] === "thunderstorms")) {
        workUmb -= 1
        homeUmb += 1
      }
    }
  }
  return homeUmb + workUmb
}



Once upon a time, on a way through the old wild west,…
… a man was given directions to go from one point to another. The directions were "NORTH", "SOUTH", "WEST", "EAST". Clearly "NORTH" and "SOUTH" are opposite, "WEST" and "EAST" too. Going to one direction and coming back the opposite direction is a needless effort. Since this is the wild west, with dreadfull weather and not much water, it's important to save yourself some energy, otherwise you might die of thirst!

How I crossed the desert the smart way.
The directions given to the man are, for example, the following:

["NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH", "WEST"].
or

{ "NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH", "WEST" };
or (haskell)

[North, South, South, East, West, North, West]
You can immediatly see that going "NORTH" and then "SOUTH" is not reasonable, better stay to the same place! So the task is to give to the man a simplified version of the plan. A better plan in this case is simply:

["WEST"]
or

{ "WEST" }
or (haskell)

[West]
or (rust)

[WEST];
Other examples:
In ["NORTH", "SOUTH", "EAST", "WEST"], the direction "NORTH" + "SOUTH" is going north and coming back right away. What a waste of time! Better to do nothing.

The path becomes ["EAST", "WEST"], now "EAST" and "WEST" annihilate each other, therefore, the final result is [] (nil in Clojure).

In ["NORTH", "EAST", "WEST", "SOUTH", "WEST", "WEST"], "NORTH" and "SOUTH" are not directly opposite but they become directly opposite after the reduction of "EAST" and "WEST" so the whole path is reducible to ["WEST", "WEST"].

Task
Write a function dirReduc which will take an array of strings and returns an array of strings with the needless directions removed (W<->E or S<->N side by side).

The Haskell version takes a list of directions with data Direction = North | East | West | South. The Clojure version returns nil when the path is reduced to nothing. The Rust version takes a slice of enum Direction {NORTH, SOUTH, EAST, WEST}.

Examples
dirReduc(["NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH", "WEST"]) => ["WEST"]
dirReduc(["NORTH", "SOUTH", "SOUTH", "EAST", "WEST", "NORTH"]) => []
See more examples in "Example Tests"
Note
Not all paths can be made simpler. The path ["NORTH", "WEST", "SOUTH", "EAST"] is not reducible. "NORTH" and "WEST", "WEST" and "SOUTH", "SOUTH" and "EAST" are not directly opposite of each other and can't become such. Hence the result path is itself : ["NORTH", "WEST", "SOUTH", "EAST"].



function dirReduc(arr){
  for (var i = 0; i < arr.length; i++) {
    if (arr[i] === "NORTH") {
      if (arr[i+1] === "SOUTH") {
        arr.splice(i, 2)
        if (i > 0) {
          i -= 2
        } else {
          i -= 1
        }
      }
    }
    if (arr[i] === "SOUTH") {
      if (arr[i+1] === "NORTH") {
        arr.splice(i, 2)
        if (i > 0) {
          i -= 2
        } else {
          i -= 1
        }
      }
    }
    if (arr[i] === "EAST") {
      if (arr[i+1] === "WEST") {
        arr.splice(i, 2)
        if (i > 0) {
          i -= 2
        } else {
          i -= 1
        }
      }
    }
    if (arr[i] === "WEST") {
      if (arr[i+1] === "EAST") {
        arr.splice(i, 2)
        if (i > 0) {
          i -= 2
        } else {
          i -= 1
        }
      }
    }
  }
  return arr
}



Write a function that when given a URL as a string, parses out just the domain name and returns it as a string. For example:

domainName("http://github.com/carbonfive/raygun") == "github" 
domainName("http://www.zombie-bites.com") == "zombie-bites"
domainName("https://www.cnet.com") == "cnet"

def domain_name(url)
  final = ""
  i = url.length - 1
  name = false
  until i < 0
    if name == true
      final = url[i] + final
      if url[i-1] == "." || url[i-1] == "/"
        name = false
      end
    end
    if url[i-3..i] == ".com" 
      i -= 3
      name = true
    end
  i -= 1
  end
  return final
end



Task
"AL-AHLY" and "Zamalek" are the best teams in Egypt, but "AL-AHLY" always wins the matches between them. "Zamalek" managers want to know what is the best match they've played so far.

The best match is the match they lost with the minimum goal difference. If there is more than one match with the same difference, choose the one "Zamalek" scored more goals in.

Given the information about all matches they played, return the index of the best match (0-based). If more than one valid result, return the smallest index.

Example
For ALAHLYGoals = [6,4] and zamalekGoals = [1,2], the output should be 1.

Because 4 - 2 is less than 6 - 1

For ALAHLYGoals = [1,2,3,4,5] and zamalekGoals = [0,1,2,3,4], the output should be 4.

The goal difference of all matches are 1, but at 4th match "Zamalek" scored more goals in. So the result is 4.

Input/Output
[input] integer array ALAHLYGoals

The number of goals "AL-AHLY" scored in each match.

[input] integer array zamalekGoals

The number of goals "Zamalek" scored in each match. It is guaranteed that zamalekGoals[i] < ALAHLYGoals[i] for each element.

[output] an integer

Index of the best match.



function bestMatch(ALAHLYGoals, zamalekGoals) {
  var final = [100000000, 1000000000, 1000000000]
  for (var i = 0; i < ALAHLYGoals.length; i++) {
    if (ALAHLYGoals[i] - zamalekGoals[i] < final[1]) {
      final = [i, ALAHLYGoals[i] - zamalekGoals[i], zamalekGoals[i]]
    } else if (ALAHLYGoals[i] - zamalekGoals[i] === final[1]) {
      if (final[2] < zamalekGoals[i]) {
        final = [i, ALAHLYGoals[i] - zamalekGoals[i], zamalekGoals[i]]
      }
    }
    console.log(i + ": " + final)
  }
  return final[0]
}





Your job is to write a function which increments a string, to create a new string. If the string already ends with a number, the number should be incremented by 1. If the string does not end with a number the number 1 should be appended to the new string.

Examples:

foo -> foo1

foobar23 -> foobar24

foo0042 -> foo0043

foo9 -> foo10

foo099 -> foo100

Attention: If the number has leading zeros the amount of digits should be considered.


def increment_string(input)
  if input.to_i != 0 
    this = (input.to_i+1).to_s
    if this.length < input.length 
      i = input.length - this.length 
      until i == 0 
        this = "0" + this
      i -= 1
      end
    end
    return this
  end
  number = ["", 0]
  i = input.length-1
  until i < 0
    if (("a".."z").include? input[i]) || (("A".."Z").include? input[i])
      number[1] = i
      i = -1
    else
      number[0] = input[i] + number[0]
    end
  i -= 1
  end
  final_num = (number[0].to_i+1).to_s
  if final_num.length < number[0].length
    i = number[0].length - final_num.length
    until i == 0
      final_num = "0" + final_num
    i -= 1 
    end
  end
  final = input[0..number[1]] + final_num
end

