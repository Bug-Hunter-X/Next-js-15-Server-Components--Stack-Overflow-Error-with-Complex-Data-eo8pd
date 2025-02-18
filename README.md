# Next.js 15 Server Components: Stack Overflow Bug

This repository demonstrates a potential bug in Next.js 15 server components related to stack overflow errors when handling deeply nested or cyclic data structures.

## Bug Description
When a server component attempts to serialize a large, complex object with circular references, it can hit the maximum call stack size, resulting in a runtime error. This is due to the recursive nature of object serialization.

## Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the error in the browser console.

## Solution
The solution involves implementing a mechanism to detect and handle circular references during serialization, preventing the infinite recursion.  This can involve using a custom serializer or leveraging libraries designed to handle complex object serialization safely.