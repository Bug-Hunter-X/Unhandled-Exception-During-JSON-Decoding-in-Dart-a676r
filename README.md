# Unhandled Exception During JSON Decoding in Dart

This repository demonstrates a common error in Dart when handling asynchronous API calls and JSON responses. The `bug.dart` file contains code that fetches data from an API and attempts to decode the JSON response.  However, it lacks proper error handling for the `jsonDecode` function.  The `bugSolution.dart` file shows the corrected version with comprehensive error handling.

## Problem

The original code does not handle the possibility of exceptions during JSON decoding (e.g., if the API returns malformed JSON). This could lead to the app crashing or failing silently.

## Solution

The improved code includes a `try-catch` block around `jsonDecode` to specifically handle `FormatException` and other potential exceptions. This provides more robust error handling and prevents unexpected crashes.