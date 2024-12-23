# React useEffect Hook Performance Issue

This repository demonstrates a common performance issue in React applications related to the `useEffect` hook. The example shows how an effect that runs after every render can lead to unnecessary re-renders and performance degradation.

## Problem

The `useEffect` hook, without proper dependency array management, runs after every render of the component.  In this example, the console log shows that it triggers after each click, even though the data is used only for display. This is inefficient. 

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array.  By only including `count` in the array, the effect only runs when the value of `count` changes.