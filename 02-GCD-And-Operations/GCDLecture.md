# Operations
  - Dependencies
  - Subclassing
  - Operation Queues
  - BlockOperations
  - GCD vs Operations
  - Differences
  - When to use


- Why?
- Describe Operations
  - Higher lever abstraction over GCD
  - Object oriented vs functions
  - Operate concurrently but can be serial by using dependencies
  - Operations describes a single unit of work
  - Operations are submitted to OperationQueues to be processed based on priority of the operation
  - There are main queue an custom queues
  - Operations is an abstract class, ie its designed to be subclassed
  - Two subclasses given are NSBlockOperation and  NSInvocationOperation-- gone
  - Subclassing operations, you can override main or start method, main is less flexible but manages state of the operation for you (e.g assumes when main returns its finished), start you have to do that manually
  - 3 Booleans, Finished, Cancelled, Ready
  - Finished completion block is called when operation is done
- Benefits
  - Can add dependencies between operations easily


- Examples, code walkthrough
  - You add dependencies with addDependency(operation: myOperation) on the Operation subclass

- When to use GCD
- Work with the most level of abstraction

# Why? 2min
# Describe operations 2
# Block Operations - 5
 - Use cases for block operations
 - completion handlers
 - more blocks
 - Examples
# Subclassing Operations - 5
# GCD vs Operations
