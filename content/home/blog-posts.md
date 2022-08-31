---
widget: pages
widget_id: RECENT-POSTS
headless: true
weight: 20
title: RTL Design
subtitle: ""
active: true
content:
  offset: 0
  order: desc
  filters:
    folders:
      - post
    tag: ""
    category: ""
    publication_type: ""
    author: ""
    exclude_featured: false
  archive:
    enable: false
design:
  columns: "1"
  view: card
  flip_alt_rows: true
  background:
    image: rtl-design-feature.png
  spacing:
    padding:
      - 0
      - 0
      - 0
      - 0
---


Involves the design/integration of digital logic modules that go into a chip or IP.

## Topics covered

* Verilog syntax and programming
* * Try to be familiar with all the synthesizable constructs used in Verilog
  * * Ex. Blocking vs Non-blocking statements - trivial, but it is surprising how often it comes up (and how often interviewees stumble)
    * Casex, Casez and the variations
  * A very common question pattern: 
  * * Write Verilog code to do “something” (Ex. BCD counter)
    * What do the different sections of your code synthesize to - very important to know this, this is where Verilog interviews are different from other coding interviews. For example, always @ (posedge clock) would typically result in a logic involving Flip-Flops
    * Make some kind of changes to the input/output (Ex. Output should be triggered by another signal, Output should be seen with a delay of one cycle, Synchronous vs Asynchronous reset, etc)
* Digital Design concepts
* * Basic logic design (the kind of questions that show up in an undergraduate digital electronics course) - Ex. Universal gates, design different gates using a MUX
  * Designing a counter is also the most commonly asked design question
  * State Machine design
  * * Design state machines (Draw the state diagram) for the given scenario
    * Mealy vs Moore model - very very important - learn how to come up with both models any scenario
    * Typically, state machine questions are converted to Verilog questions (i.e. write verilog code for the state machine you designed). It is good to practice a template for state machines (both models) so that you can convert any state diagram to code easily.
    * Another variation here could be binary encoding vs one-hot encoding for the states - each has pros and cons
* Static Timing Analysis
* * What the different terms (setup time, hold time, etc) mean
  * Given a Flop - Logic - Flop configuration
  * * Is there setup or hold violations
    * If there are any, how to fix them
    * There are multiple variations of this question, and they are well documented in any STA book or tutorial - spend time to master this
  * Time borrowing (Especially if you are a grad student)
  * Metastability and how to deal with it