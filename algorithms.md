# [fit] Algorithms, not Al Gore's Rhythm

![inline autoplay mute loop](assets/algore.gif)

---

# About Me

---

![fit](assets/TIIY-Logo-500px-white.png)

^ Instructor at The Iron Yard

---

![fit](assets/riley.png)

^ I have promised my girlfriend that I would include a photo of our dog Riley in each presentation I do.

^ I am the Backend Instructor here at The Iron Yard.

---

# retail

![fit](assets/checkout.jpg)

^ Out of school I worked for a consulting company that reviewed, recommended, and installed systems for POS, inventory management, warehouse management, and financial control for retail

---

# telephony

![fit](assets/switchboard-operator.jpg)

^ Have built software, and embedded systems, to manage remote PBXs (e.g. the large corporate phone systems)

---

# space

![fit](assets/BMRST.png)

^ Worked in the aerospace industry on command-destruct systems for rocket launches

---

# signage

![fit](assets/Real-Digital-Media-Rave-Cinemas-Digital-1.jpg)

^ Built digital signage systems using Rails, Content Distribution Systems, and a custom Linux OS for embedded devices

---

# Algorithms

^ Like any good presentation lets give the boring definition

---

> Self-contained step-by-step set of operations to be performed.

^ And another definition...

---

> Algorithms perform calculation, data processing, and/or automated reasoning tasks.

^ And another definition...

---

> An algorithm is an effective method that can be expressed within a finite amount of space and time and in a well-defined formal language for calculating a function.

^ And another definition...

---

![fit](assets/mindblown.gif)

^ WHAAAAAT?

---

# [fit] We use them in life all the time

---

# [fit] Examples

---

![fit](assets/map.png)

^ Giving specific directions to someone on how to drive from place to place

^ Going to come back to directions later.

---

#### http://bit.ly/1tsqopI

![inline fill](assets/recipe.jpg)

^ Followed, created, or modified a recipe for cooking

---

#### http://bit.ly/1Pp7bZY

![inline fill](assets/ikea.jpg)

^ "Place Tab A into Slot B"

---

![fit](assets/owl.jpg)

^ Draw two circles

^ Draw the rest of the damn owl

---

# [fit] More formal

^ These are casual examples of algorithms we use or create all the time

^ Time to bring back that horror of high school math: Geometry

---

![fit](assets/bisect.png)

^ Formal construction for bisecting the angle

---

# Euclid's Algorithm for GCD

```ruby
while (A != B) {

 if (A > B)
   A = A - B
 else
   B = B - A

}

return A
```

---

# Euclid's Algorithm for GCD

`A = 210, B = 45`

---


# Euclid's Algorithm for GCD

`A = 210, B = 45`
<br>
`A > B (210 > 45)`
<br>
`A = 210 - 45`
<br>
`A = 165`

---

# Euclid's Algorithm for GCD

`A = 165, B = 45`

---

# Euclid's Algorithm for GCD

`A = 165, B = 45`
<br>
`A > B (165 > 45)`
<br>
`A = 165 - 45`
<br>
`A = 120`

---

# Euclid's Algorithm for GCD

`A = 120, B = 45`

---

# Euclid's Algorithm for GCD

`A = 120, B = 45`
<br>
`A > B (120 > 45)`
<br>
`A = 120 - 45`
<br>
`A = 75`

---

# Euclid's Algorithm for GCD

`A = 75, B = 45`

---

# Euclid's Algorithm for GCD

`A = 75, B = 45`
<br>
`A > B (75 > 45)`
<br>
`A = 75 - 45`
<br>
`A = 30`

---

# Euclid's Algorithm for GCD

`A = 30, B = 45`

---

# Euclid's Algorithm for GCD

`A = 30, B = 45`
<br>
`else ... since it isn't true that (30 > 45)`
<br>
`B = 45 - 30`
<br>
`B = 15`

---

# Euclid's Algorithm for GCD

`A = 30, B = 15`

---

# Euclid's Algorithm for GCD

`A = 30, B = 15`
<br>
`A > B (30 > 15)`
<br>
`A = 30 - 15`
<br>
`A = 15`

---

# Euclid's Algorithm for GCD

`A = 15, B = 15`

---

# Euclid's Algorithm for GCD

`A = 15, B = 15`
<br>
`done with *while* since A == B`
<br>
`GCD = 15`

---

# [fit] Must be precise and complete

---

# [fit] "Make a PB&J Sandwich"

^ Give a couple of example tries

^ Show that nearly every step we think is precise, could be more precise

^ Suggest people try at home

---

# [fit] This is the :key: to mastering programming

---

![fit](assets/break-it-down.jpg)

^ When starting out with algorithms, the more detail we include, even to the point where it may seem silly, the better developers we will be.

---

    1. Read the problem completely twice.
    2. Solve the problem manually with 3 sets of sample data.
    3. Optimize the manual steps.
    4. Write the manual steps as comments or pseudo-code.
    5. Replace the comments or pseudo-code with real code.
    6. Optimize the real code.

^ https://simpleprogrammer.com/2011/01/08/solving-problems-breaking-it-down/

---

# Read the problem completely twice.

    - Most important!
    - Can you explain it (simply) to someone else?

---

# Solve the problem manually

    - Programming is automation
    - Solve the problem manually
    - Maybe even on pen and paper
    - Or use physical objects
    - Practice!

---

# Optimize the manual solution

    - Can you remove steps?

---

# Write pseudo-code or comments

    - Open an editor and write the manual steps in English

---

# Replace comments with real code

    - Replace each individual steps with code

---

# Example

-
-
-
-

## [fit] Reverse a string (word)

^ Our goal is to be able to reverse any string (word)
^ How would we break this down into tiny steps

---

    1. Write “Zebra” down.
    2. Create a new empty word.
    2. Start at the last letter in the word (the "a" from Zebra)
    3. Put the current letter at the end of the new word
    4. If there is a previous letter,
       make the previous letter the current letter
       letter and start back at 3.
    5. When there are no more letters in the word, our
       new word is the answer.
---

# Pseudo code

    1. NewWord = ""
    2. Loop backwards through word to reverse
    3.   NewWord += CurrentLetter
    4. Return NewWord

---

# Code (Ruby)

```ruby
word = "Zebra"

new_word = ""
word.chars.reverse_each do |letter|
  new_word += letter
end

new_word # => "arbeZ"
```

---

# Sorting!

---

# [fit] Simplest Sorting EVAR

---

# Bubble sort

![fill](assets/bubbles.jpg)

^ https://www.flickr.com/photos/shannonlofthus/4670090955/in/photolist-87Frkz-WHY5B-8mahpK-hN6juM-r7AJpA-ajYWaD-6zd2fV-nhgRbE-86k6Pf-38z42x-indd8g-o92k4j-btkhTp-8as94X-gdM5mg-nuoPxX-8ibJQ1-h2paWu-rqZ7-2wtUmq-7LYqqC-7yGiBn-2VD8P9-bWUbbw-6dXEed-ayCXtz-9VZvt5-ah6cUm-7aNK5e-dM9tRD-bytmvQ-fdgM3t-fMGVce-oDBmtB-fpCiAy-9GxMTc-iALYdC-9gcyYE-e5xtKs-xYMme-5TBqfJ-etJxvL-9TRW6k-4ZPTPC-9JtZ4F-96g9Ms-anRjkS-cqPJ9b-aqFvbJ-85xV3n

---

> For each two adjacent elements

<br>

> Exchange them if out of order

<br>

> Repeat until array is sorted.

---

# Break it down

    1. Assume the array is sorted

    2. Go through each pair of elements
       - If the first is larger than the second
         - Swap the two elements
         - Remember that the array isn't sorted

    3. When done with all the elements, if we
       still believe the array is sorted, STOP

    4. Otherwise go back to step 1

---

^ explain ... in range

^ explain each_cons

```ruby
array = [7,1,2,9,4,5]

def bubble_sort(array)
  loop do
    sorted = true
    (0...array.length).each_cons(2) do |first, second|
      if array[first] > array[second]
        array[first], array[second] = array[second], array[first]
        sorted = false
      end
    end
    break if sorted
  end
end
```

---
![inline autoplay mute loop](assets/bubblesort.mp4)

- https://github.com/AIRTucha/SortVis

---

### A moment of zen

![fit](assets/zen-garden.jpg)

^ https://www.flickr.com/photos/91604813@N03/8439070389/in/photolist-dRJrBB-s4K1VU-p6DwNY-dRQ271-csLT6L-s5HH9C-53sRLW-p6GeRy-edcCWC-nWCE27-nv6aQE-anoGck-anoFKK-7ius6w-sntwEE-nHEyJ7-anrLr1-ay5Dmf-eijpgL-eimZwd-eidF5v-ekmQMh-anrBX9-dRJrCg-anxCHQ-53oCGD-ay2W6B-54vk5W-anuNNk-anoDX8-anrKnG-dH8fwH-qanAxd-ay5DCW-8VRU3W-poMWLN-ekmnqN-fy8aDK-G78Jjz-anrJWw-anrKLb-anoYUR-5oUwi3-eidEGz-eijpkb-g4cW9M-ein3Yy-eidEQV-b6uVeB-a6v8Lx

^ Moment of zen

---

# [fit] Algorithm Complexity

^ How do we know how "good" or algorithm is?

---

# Measure
- the number of operations required => _time_
- the amount of memory required     => _space_

---

> Best case
-
-
> Worst case
-
-
> Average case
-
-

^ Best case - if the data is perfect for *this* algorithm, how fast
  Worst case - if the data is terrible for *this* algorithm, how slow
  Over all possible inputs, what is the average speed of the algorithm

---

# What are we measuring?

^ TODO: Maybe mention Turing Machine here?

^ When we speak of algorithm complexity, what are we measuring?
  Operations: comparisons, increments.

---

# Example: Searching

---

![fit](assets/binary-and-linear-search-animations.gif)

^ Binary search we half the amount of comparisons we need to do
  each time we make a decision. This is worst case log(n)

^ The linear search has to compare every element until it finds it.
  Worst case is O(n)

---

# [fit] Big O notation

---

> `O(1)`
> `O(n)`
> `O(log n)`
> `O(n log n)`
> `O(n^2)`
> `O(2^n)`

- These grow at a different rate based on how `n` changes

---

> `O(1)`

    Takes a constant amount of time regardless of input size

    Example: looking up an index in an array
             looking up a key in a hash/dictionary (most cases)

---

> `O(n)`

    If n doubles, the algorithm takes twice as long

    Example: linear search animation

---

> `O(n^2)`

    If n doubles, the algorithm takes FOUR times as long

    Example: bubble sort!

---

> `O(2^n)`

    If n doubles, the algorithm takes many times as long

    e.g. if n grows from 20 to 40, O(2^n) grows by over a MILLION times

---

# Tower of Hanoi

    The Tower of Hanoi is a mathematical game or puzzle.

    It consists of three rods and a number of disks
    of different sizes, which can slide onto any rod.

    The puzzle starts with the disks in a neat stack
    in ascending order of size on one rod, the smallest
    at the top, thus making a conical shape.

---

# Tower of Hanoi

    The objective of the puzzle is to move the entire

    stack to another rod, obeying simple rules

---

# Tower of Hanoi

    1. Only one disk can be moved at a time.

    2. Each move consists of taking the upper disk
       from one of the stacks and placing it on top
       of another stack i.e. a disk can only be
       moved if it is the uppermost disk on a stack.

    3. No disk may be placed on top of a smaller disk.

---

# [fit] Tower of Hanoi

# $$ 2^n $$

---

# [fit] Tower of Hanoi

![right fit](http://see-math.math.tamu.edu/2010/CounselorMovies/philip-y.gif)

---

# [fit] To understand recursion you
# [fit] must first understand recursion

---

# Tower of Hanoi

<br>

## If we could move a disk per second
## how long would this take?

---

Disks   | Time | |
------- | ----- | --- |
_1_     | **less than a minute** | |
_8_     | **4 minutes** | |
_12_    | **about 1 hour** | |
_17_    | **1 day** | |

^ Up to about a day

---

Disks   | Time | |
------- | ----- | --- |
_21_    | **24 days** | |

^ Up to about a month

---

Disks   | Time | |
------- | ----- | --- |
_25_    | **about 1 year** | |

^ Up to about a year

---

Disks   | Time | |
------- | ----- | --- |
_31_    | **about 68 years** | |

^ Up to about an (average) lifetime

---

Disks   | Time | |
------- | ----- | --- |
_35_    | ... **over 1,089 years** | |

^ Up to about a millennium

---

Disks   | Time | |
------- | ----- | --- |
_50_    | **35.7 million years** :scream: | |

^ ZOMG

---

# [fit] Complexity

---

![fit](assets/complexity.jpg)

---

## Salesperson

![fit](assets/1955_Mercury_Montclair_Convertible.jpg)

^ Imagine you are a traveling salesperson.

---

![fit](assets/Sicily-cities-map-bjs.jpg)

^ What is the best route for the salesperson to visit each city only once, returning to the starting city at the end?

---

# [fit] Could you find it by hand?

---

# [fit] Probably, for a small number of cities!

---

# 1 Billion Computations per second

Cities | Time
------ | ----
2      | less than a minute
3      | less than a minute
4      | less than a minute
14     | 1 minute
16     | about 6 hours

---

# 1 Billion Computations per second

Cities | Time
------ | -----------------
18     | 2 months
19     | almost 4 years
21     | about 1,620 years

---

![fit](assets/tsp_iteration.gif)

^ Upwards of 400,000 iterations for about 50 cities

---

# The TSP has several applications

    planning


    logistics


    manufacturing of microchips


    DNA sequencing

---

# [fit] For More info

# [fit] http://bit.ly/XUXLXWX

---

# [fit] Wrap It Up

![fit autoplay mute loop](assets/wrap-it-up.gif)

^ Lets wrap this up

---

# [fit] Algorithms Matter

---

# [fit] Understanding Complexity Matters

---

## Understanding How to Break Problems Down Effectively **REALLY Matters**

---

# Being a Developer

    1. Understanding the problem
    2. Break it down into small steps
    3. Break it into even smaller steps
    4. Translate this to code
    5. Appreciate the complexity

---

# How to practice?

    exercism.io


    codewars.com


    CoderNight meetup
    (http://meetup.com/CoderNight)

---

# [fit] Thank You

---

# [fit] Questions?
