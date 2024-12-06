# Stack Overflow in ActionScript 3 Caused by Long Comments

This repository demonstrates a bug in older versions of the Adobe Flash Player where excessively long comments in ActionScript 3 code can lead to a stack overflow error.  This issue is related to the internal handling of comments by the Flash Player's compiler or interpreter.

## Problem

When using extremely long single-line or multi-line comments, the Flash Player may encounter a stack overflow error, resulting in a crash or unexpected behavior of the application. This appears more commonly in older versions of Flash Player, which may have limitations in their parsing of very long comments.

## Solution

The solution is to refactor the code and avoid excessively long comments. Breaking down lengthy comments into smaller, more manageable chunks prevents this issue. The use of external documentation instead of extensive in-code comments for complex logic is often a superior practice.

## How to reproduce

1. Clone the repository.
2. Open the `bug.as` file. You'll see a very long comment.
3. Attempt to compile or execute this file using an older Flash Player version (e.g., Flash Player 10).  A stack overflow error or similar exception should occur.
4.  Compare this with the `bugSolution.as` file, where the comment is split into smaller, manageable sections to show the fix. 