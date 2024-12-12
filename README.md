# Elixir Enum.each and Process.exit Bug

This repository demonstrates a subtle bug that can occur when using `Enum.each` in Elixir in conjunction with `Process.exit`. The code attempts to iterate over a list and print each element, but prematurely exits due to an improperly placed `Process.exit` call within the loop.  This example highlights the importance of understanding the implications of `Process.exit` within concurrent contexts.

## How to Reproduce
1. Clone the repository.
2. Run the `bug.ex` file.
3. Observe that the process terminates before printing all elements of the list.

## Solution
The solution replaces `Enum.each` with `Enum.map` or refactors the logic to avoid premature termination of the process. The solution file, `bugSolution.ex`, provides an alternative implementation.