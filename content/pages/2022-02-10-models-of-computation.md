<!-- title: How the Discrete Emerges from the Continuous -->
<!-- date: 2022-02-10 -->


As humans, we like to categorize continuous things into discrete categories.
I used to think how arbitrary it is to set artifical thresholds over a continuous metrics in order to segment the world into discrete categories.
For instance, a man would be considered tall if he is taller than 6 foot, short if he is shorter than 5 feet, and average height in between those thresholds.
Same thing for many adjectives, often coming in opposites, such as "rich/poor", "fat/skinny", "pretty/ugly", "cheap/expensive".
Same thing for colors: "red, orange, yellow, green, blue, violet" are more or less wavelength ranges inside the visible spectrum.

Sure, those categories and stereotypes come in handy, but is there more to it?


Turns out, sometimes there are fundamental differences betweem the categories. For instance, at usual atmospheric pressures, the distinction between ice, liquid water, and water vapor is pretty clear.
The distinction is not merely about segmenting the temperature scale at 0 (32F) and 100 (212F) degrees Celsius, but their physical properties are fundamentally different, and can be experienced firsthand with our senses. The transition from one category to another is referred to as <a href="https://en.wikipedia.org/wiki/Phase_transition">phase transitions</a>, which is a term that has wide use beyond physics. Below, we will explore the notion of exponential scalability of different categories of computational models.
Not sure, but there might be some loose analogies to make  with  <a href="https://en.wikipedia.org/wiki/Critical_exponent">critical exponents</a> which can be used to characterize phase transitions.

Another example from automata theory. I learned in class about how a <a href="https://en.wikipedia.org/wiki/Turing_machine">Turing machine</a> is a strictly stronger computational model than a <a href="https://en.wikipedia.org/wiki/Finite-state_machine">finite-state machine</a> (FSM). 
That means the Turing machine can do things that a FSM can, like recognizing regular expressions, but also do things that the FSM cannot do, such as computing the result from an arbitrary piece of Python code. 
The (deterministic) Turing machine is modeled as a FSM which has the option of moving along an infinite tape (like a RAM) and can read or write predefined symbols (say, 8-bit bytes).
Technically, following this definition, any physical computer is not a Turing machine, because it has finite memory instead of an infinite tape.
Instead, any computer can be modeled by a FSM, with number of states roughly <i>exponential</i> in the RAM (tape) size, say, 2 to the power 8,000,000,000.
However, in practice, as long as we don't exceed the RAM limit, the computer acts and behaves like a Turing machine.
So maybe, a more practical definition of FSMs would be to restrict them to a non-exponential, reasonable number of states.
The scaling of the number of FSM states with respect to the length of the tape size

Analogously, decision problems are often categorized in <a href="https://en.wikipedia.org/wiki/NP-hardness">NP-hard</a> (non-deterministic polynomial hard) vs. P (polynomial). 
P problems can be solved in polynomial time by a determinstic Turing machine.
NP-hard problems, are defined as ones that can be solved in polynomial time by a non-deterministic Turing machine (e.g. quantum computer). Examples of NP-hard problems are the traveling salesman problem (applications in operations research), and prime factorization (applications in cryptography), or bitcoin mining.
Given enough time, NP-hard problems by deterministic Turing machines (regular computers), at the cost of spending an exponential amount of time in the problem.
Here again, the exponential asepect, in terms of computational time, is the key. In fact, quantum computers will reamin weaker computional machines than regular computers, as long as they cannot scale to problem sizes large enough for which the scalability matters.


