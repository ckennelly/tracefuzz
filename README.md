tracefuzz - A Trace-Driven Fuzz Tester
(c) 2013 - Chris Kennelly (chris@ckennelly.com)

Overview
========

tracefuzz instruments a binary and generates test cases for it.  As these tests are executed, traces of instructions are built up.  From these, tracefuzz generates further test cases to explore unvisited instructions and branches.  Additionally, this approach allows the space of system call return values to be explored.  \verb/malloc/ may return \verb/NULL/ and an IO operation may fail.  These error injections may uncover further faults for which no branches exist, as the error is improperly handled.
