# React useEffect Infinite Loop

This repository demonstrates a common React bug: an infinite loop caused by improperly using the `useEffect` hook. The component continuously updates its state, leading to an infinite render cycle.

## Bug Description

The `useEffect` hook attempts to increment the `count` state variable within its dependency array.  Because `count` is a dependency, the effect function will be executed every time `count` changes, leading to an infinite loop of state updates.

## Solution

The solution is to avoid directly modifying the `count` state variable within the `useEffect`'s body. Instead, use a flag or conditional logic to manage when the state updates.