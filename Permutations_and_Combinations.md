# Permutations and Combinations

**Author: Shekh Mostofa Abedin**

## Permutations

### Key Concepts:

1. **Permutation Formula:**

   - **General Permutation Formula:**
     \[
     P(n, k) = \frac{n!}{(n-k)!}
     \]

     - \( n \) is the total number of items.
     - \( k \) is the number of items to arrange.

   - **Example:**
     If you have 5 distinct objects and you want to arrange 3 of them, the number of permutations is:
     \[
     P(5, 3) = \frac{5!}{(5-3)!} = \frac{5!}{2!} = \frac{120}{2} = 60
     \]
     There are 60 different permutations of selecting 3 objects from a set of 5 distinct objects.

2. **Permutations of \( n \) Distinct Objects:**

   - When all objects in a set are distinct, the number of permutations is simply the factorial of the total number of objects:
     \[
     P(n) = n!
     \]
   - **Example:**
     For 4 distinct objects:
     \[
     P(4) = 4! = 24
     \]
     There are 24 different ways to arrange 4 distinct objects.

3. **Circular Permutations:**

   - In circular permutations, the arrangement forms a closed loop, meaning the first and last elements are adjacent.
   - The formula is:
     \[
     P\_{\text{circular}}(n) = (n-1)!
     \]
   - **Example:**
     For 5 distinct objects arranged in a circle:
     \[
     P\_{\text{circular}}(5) = 4! = 24
     \]
     There are 24 different circular permutations of arranging 5 distinct objects.

4. **Permutations with Repetition:**

   - If some objects are repeated, the permutation formula is adjusted to account for the repetitions:
     \[
     P\_{\text{repetition}}(n, k_1, k_2, \ldots, k_r) = \frac{n!}{k_1! \times k_2! \times \ldots \times k_r!}
     \]
   - **Example:**
     Arranging the letters in the word "BOOK":
     \[
     P\_{\text{repetition}}(4, 1, 2, 1) = \frac{4!}{1! \times 2! \times 1!} = \frac{24}{2} = 12
     \]
     There are 12 different ways to arrange the letters in "BOOK".

5. **Permutation with All Items:**

   - When all items are taken (\( k = n \)), the permutation simplifies to:
     \[
     P(n, n) = n!
     \]
   - **Example:**
     For 4 objects:
     \[
     P(4, 4) = 4! = 24
     \]

### Edge Cases in Permutations

**Permutations with Constrained Positions:**

- **Scenario:** When certain items must remain together or in specific positions.
- **Example:** Arranging 4 vowels and 3 consonants in a row, where the consonants must be together.
  - **Steps:**
    1.  Treat the group of consonants as a single unit.
    2.  Arrange the units, then arrange the items within the unit.
  - **Calculation:**
    \[
    \text{Total Arrangements} = (n-k+1)! \times k!
    \]
    - For 4 vowels and 3 consonants (consonants together):
      \[
      5! \times 3! = 120 \times 6 = 720
      \]
      So, there are 720 different ways to arrange the letters.

---

## Combinations

### Key Concepts:

1. **Combination Formula:**

   - **General Combination Formula:**
     \[
     C(n, k) = \frac{n!}{k! \times (n-k)!}
     \]

     - \( n \) is the total number of items.
     - \( k \) is the number of items to select.

   - **Example:**
     If you have 6 different books and want to select 3 to read:
     \[
     C(6, 3) = \frac{6!}{3! \times (6-3)!} = \frac{720}{6 \times 6} = 20
     \]
     There are 20 different combinations of selecting 3 books from a set of 6 books.

2. **Combination with All Items:**

   - When all items are selected (\( k = n \)), the combination simplifies to:
     \[
     C(n, n) = 1
     \]
   - **Example:**
     If selecting all 4 objects from a set of 4:
     \[
     C(4, 4) = 1
     \]

### Edge Cases in Combinations

1. **Selecting Items with One Predefined Position:**
   - **Scenario:** Selecting a subset where one item must be in a specific position, such as a chairperson in a committee.
   - **Example:** Selecting 4 people from a group of 12, where one person must be the chairperson.
     - **Steps:**
       1. Select the chairperson first.
       2. Select and arrange the remaining people.
     - **Calculation:**
       \[
       \text{Total Selections} = n \times C(n-1, k-1)
       \]
       - For selecting 4 people with a chairperson:
         \[
         12 \times C(11, 3) = 12 \times 165 = 1980
         \]
         So, there are 1,980 different ways to form the committee.

## How to Distinguish Between Permutations and Combinations

### **Permutation Keywords (Order Matters)**

1. **"Arrange"**: When the problem involves arranging items, the order is important, so it's a permutation problem.

   - **Example**: "How many different ways can you arrange the letters in the word 'UNIQUE'?"

2. **"Order"**: If the order in which the items are arranged matters, it’s a permutation.

   - **Example**: "How many different orders can you create with these 5 people?"

3. **"Line up" or "Position"**: If people or items are being lined up or placed in a specific position, the problem is about permutations.

   - **Example**: "In how many ways can you line up 4 people?"

4. **"Permutations"**: If the problem directly mentions "permutations," then it’s obviously a permutation problem.

   - **Example**: "Calculate the permutations of selecting 3 items out of 5."

5. **"Sequence"**: When the order in which items appear is important.

   - **Example**: "Find the number of possible sequences of letters."

6. **"Rank"**: When the problem asks for a specific rank or position within an ordered list.

   - **Example**: "What is the rank of the word 'MATH' in all possible arrangements?"

7. **"Placement"**: When placing items or people in specific positions or slots.

   - **Example**: "Determine the number of placements of 4 people in 6 chairs."

8. **"Line" or "Row"**: When items or people are arranged in a line or row, indicating that order is important.

   - **Example**: "In how many ways can you arrange these items in a row?"

9. **"Schedule"**: When events or tasks are arranged in a particular order.

   - **Example**: "How many ways can you schedule 5 meetings?"

10. **"Permutations of"**: Often used to indicate that the problem is asking for the number of permutations of a certain number of items.

    - **Example**: "Find the number of permutations of 3 out of 8 objects."

11. **"Line-up"**: Specifically when people or objects are lined up in a particular order.

    - **Example**: "In how many ways can you line-up these players?"

12. **"Combination lock"**: Despite the term "combination," the concept of a combination lock often involves permutations because the order of numbers matters.

    - **Example**: "How many different combination locks can be made with 4 digits?"

13. **"Tournament"**: When the order of games or matches matters.
    - **Example**: "In how many ways can a tournament of 8 teams be organized?"

### **Combination Keywords (Order Doesn’t Matter)**

1. **"Select"**: If the problem involves selecting items without regard to order, it’s a combination problem.

   - **Example**: "In how many ways can you select 3 students from a group of 10?"

2. **"Choose"**: Like "select," if you are choosing items and the order doesn’t matter, it’s a combination.

   - **Example**: "How many ways can you choose 4 books from a shelf of 12?"

3. **"Committee"**: Problems involving forming a committee where the positions are not important usually refer to combinations.

   - **Example**: "In how many ways can a committee of 5 be formed from 20 people?"

4. **"Subset"**: If you are forming a subset from a larger set, and the order doesn’t matter, it’s a combination problem.

   - **Example**: "How many different subsets of size 3 can be created from a set of 8 elements?"

5. **"Combinations"**: If the problem mentions "combinations," it’s a combination problem.

   - **Example**: "Calculate the combinations of selecting 4 items from a set of 10."

6. **"Group"**: Forming a group where the arrangement within the group doesn’t matter.

   - **Example**: "How many ways can a group of 3 be formed from 7 people?"

7. **"Team"**: Selecting a team where positions within the team don’t matter.

   - **Example**: "How many ways can you form a team of 5 from 10 people?"

8. **"Sample"**: When drawing a sample from a larger population where the order doesn’t matter.

   - **Example**: "How many different samples of 4 can be drawn from a group of 20?"

9. **"Partition"**: Dividing a set into groups or parts where the order of parts doesn’t matter.

   - **Example**: "In how many ways can you partition a set of 10 objects into two groups?"

10. **"Collection"**: Gathering items where the order doesn’t matter.

    - **Example**: "How many ways can you form a collection of 5 items from 12 available items?"

11. **"Choose from"**: When you are asked to choose from a set, often implying combinations.

    - **Example**: "In how many ways can you choose from 10 different books?"

12. **"Lottery"**: Often involves selecting numbers where the order doesn’t matter.

    - **Example**: "How many different lottery combinations can be made from 49 numbers?"

13. **"Combination of"**: Similar to "choose from," explicitly asks for combinations.

    - **Example**: "Find the number of combinations of 5 out of 15 objects."

14. **"Selection"**: When selecting items from a set where the order doesn’t matter.

    - **Example**: "How many ways can you make a selection of 3 items from 10?"

15. **"Draw"**: When drawing items from a set, implying combinations if the order doesn’t matter.
    - **Example**: "How many ways can you draw 4 cards from a deck of 52?"

### **Summary of Key Identifiers**

- **Permutation** (Order Matters): arrange, order, line up, position, sequence, rank, placement, line, row, schedule, line-up, tournament, combination lock.
- **Combination** (Order Doesn’t Matter): select, choose, committee, subset, combinations, group, team, sample, partition, collection, choose from, lottery, selection, draw.
