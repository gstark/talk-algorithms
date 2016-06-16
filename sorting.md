# [fit] Sorting and Algorithms

-
-
-
-

### Gavin Stark

---

# About Me

---

![fit](riley.png)

^ I have promised my girlfriend that I would include a photo of our dog Riley in each presentation I do.

^ I am the Backend Instructor here at The Iron Yard.

---

# space

![fit](http://www.inspace21.com/Backbone/BMRST.png)

^ Worked in the aerospace industry on command-destruct systems for rocket launches

---

# signage

![fit](http://www.digitalavmagazine.com/wp-content/uploads/2012/02/Real-Digital-Media-Rave-Cinemas-Digital-1.jpg)

^ Built digital signage systems using Rails, Content Distribution Systems, and a custom Linux OS for embedded devices

---

# Sorting

^ Today we are going to talk about sorting of data

---

# Why Sorting?
- Present lists in order
- Makes searching easier
- Merging/detecting sequences

---

# Algorithms

^ But before we can talk about how sorting works we need to discuss the concept of Algorithms

^ So like any good presentation lets give the boring definition

---

> Self-contained step-by-step set of operations to be performed.

---

> Algorithms perform calculation, data processing, and/or automated reasoning tasks.

---

> An algorithm is an effective method that can be expressed within a finite amount of space and time and in a well-defined formal language for calculating a function.

---

![fit](mindblown.gif)

^ WHAAAAAT?

---

# [fit] We use them in life all the time

---

# [fit] Examples

---

![fit](map.png)

^ Giving specifc directions to someone on how to drive from place to place

^ Going to come back to directions later.

---

#### http://bit.ly/1tsqopI

![inline fill](recipe.jpg)

^ Followed, created, or modified a recipe for cooking

---

#### http://bit.ly/1Pp7bZY

![inline fill](ikea.jpg)

^ "Place Tab A into Slot B"

---

![fit](owl.jpg)

^ Draw two circles

^ Draw the rest of the damn owl

---

# [fit] More formal

^ These are casual examples of algorithms we use or create all the time

^ Time to bring back that horror of high school math: Geometry

---

![fit](bisect.png)

^ Formal construction for bisecting the angle

---

# Euclid's Algorithm for GCD

```C
while (A != B) {

 if (A > B)
   A = A - B
 else
   B = B - A

}

return A
```

^ Try an example on a whiteboard:
  GCD of (a) 210, (b) 45
    A > B (210 > 45) => A = 210 - 45 => 165
    A > B (165 > 45) => A = 165 - 45 => 120
    A > B (120 > 45) => A = 120 - 45 => 75
    A > B (75 > 45) => A = 75 - 45 => 30
    else  (30 > 45) => B = 45 - 30 => 15
    A > B (30 > 15) => A = 30 - 15 => 15
    A == B (15 == 15) => 15

---

# [fit] Must be precise and complete

---

# [fit] "Make a PB&J Sandwich"

^ Try this out on the whiteboard

^ Show that nearly every step we think is precise, could be more precise

---

# [fit] This is the :key: to mastering programming

^ Get good at breaking down problems

---

# Sorting!

---

# [fit] Simplest Sorting EVAR

---

# Bubble sort

![fill](bubbles.jpg)

^ https://www.flickr.com/photos/shannonlofthus/4670090955/in/photolist-87Frkz-WHY5B-8mahpK-hN6juM-r7AJpA-ajYWaD-6zd2fV-nhgRbE-86k6Pf-38z42x-indd8g-o92k4j-btkhTp-8as94X-gdM5mg-nuoPxX-8ibJQ1-h2paWu-rqZ7-2wtUmq-7LYqqC-7yGiBn-2VD8P9-bWUbbw-6dXEed-ayCXtz-9VZvt5-ah6cUm-7aNK5e-dM9tRD-bytmvQ-fdgM3t-fMGVce-oDBmtB-fpCiAy-9GxMTc-iALYdC-9gcyYE-e5xtKs-xYMme-5TBqfJ-etJxvL-9TRW6k-4ZPTPC-9JtZ4F-96g9Ms-anRjkS-cqPJ9b-aqFvbJ-85xV3n

---

> For each two adjacent elements:

> Exchange them if out of order

> Repeat until array is sorted.

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

# [fit] For each element, find the place in the list
# [fit] where it belongs and "insert" it there

---

# Insertion Sort

- Assume the first element is already sorted
- Working backwards, if the previous element is smaller,
   stop as we know where to place this element, otherwise swap the element and move left.

---

^ Show how this works visually

```ruby
def insert_sort(array)
  (1...array.length).each do |pos|
    while pos > 0 &&
         array[pos-1] > array[pos]

       array[pos], array[pos-1] = array[pos - 1], array[pos]

       pos = pos - 1
    end
  end
end
```

---

# Quick Sort

^ Widely used
  Complex to understand
  Generally one of the more efficient
  Might not *always* be the best choice

---

```ruby
def quicksort(array, low = 0, high = array.length - 1)
  return unless low < high
  pivot = array[high]
  i = low
  (low...high).each do |j|
    if array[j] <= pivot
      array[i], array[j] = array[j], array[i]
      i = i + 1
    end
  end
  array[p], array[high] = array[high], array[i]
  quicksort(array, low, i - 1)
  quicksort(array, i + 1, high)
end
```

^ https://github.com/AIRTucha/SortVis

---

# [fit] Algorithm Complexity

---

- Measure of order of the number of operations required

> Best case
> Worst case
> Average case

^ Best case - if the data is perfect for *this* algorithm, how fast
  Worst case - if the data is terrible for *this* algorithm, how slow
  Over all possible inputs, what is the average speed of the algorithm

---

# What are we measuring?

^ When we speak of algorithm complexity, what are we measuring?
  Operations: comparisons, increments.

---

# Example: Searching

---

![fit](binary-and-linear-search-animations.gif)

^ Binary search we half the amount of comparisons we need to do
  each time we make a decision. This is worst case log(n)

^ The linear search has to compare every element until it finds it.
  Worst case is O(n)

---

# [fit] Big O notation

---

> O(n)
> O(n^2)
> O(log n)
> O(n log n)

---

![fit](complexity.jpg)

---

## Salesperson

![fit](1955_Mercury_Montclair_Convertible.jpg)

---

![fit](Sicily-cities-map-bjs.jpg)

^ What is the best route for the salesperson to visit each city only once, returning
  to the starting city at the end?

---

# [fit] Could you find it by hand?

---

# [fit] Probably, for a small number of cities!

---

![fit](tsp_iteration.gif)

^ Upwards of 400,000 iterations for about 50 cities

---

> The TSP has several applications even in its purest formulation, such as planning, logistics, and the manufacture of microchips. Slightly modified, it appears as a sub-problem in many areas, such as DNA sequencing.

---

# [fit] For More info

# [fit] http://bit.ly/XUXLXWX

---

# [fit] Algorithms Matter

---

# [fit] Understanding Complexity Matters

---

## Understanding How to Break Problems Down Effectively Matters

---

# Being a Developer

1. Understanding the problem
2. Breaking it down into small steps
3. Appreciate the complexity

---

# [fit] Thank You

---

# [fit] Questions?
