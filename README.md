# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications involving asynchronous network requests and JSON decoding. The initial `bug.dart` file contains code that does not gracefully handle the `FormatException` that can occur if `jsonDecode` encounters invalid JSON.  The corrected code in `bugSolution.dart` demonstrates a robust way to handle this error.

## Bug Description

The `fetchData` function attempts to fetch data from a remote API, parse it as JSON, and handle potential errors. However, it fails to catch the `FormatException` thrown by `jsonDecode` if the API returns malformed JSON. This results in a crash.

## Solution

The solution involves adding a `try-catch` block specifically to handle the `FormatException` during JSON decoding. This prevents the app from crashing and allows for more graceful error handling.