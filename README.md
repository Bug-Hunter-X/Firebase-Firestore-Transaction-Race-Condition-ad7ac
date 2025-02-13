# Firebase Firestore Transaction Race Condition

This repository demonstrates a common error in Firebase Firestore: race conditions during transactions.  When multiple clients attempt to update the same document concurrently using transactions, the outcome can be unpredictable, potentially leading to data loss or inconsistencies.

The `bug.js` file showcases the flawed code, while `bugSolution.js` provides a corrected version using optimistic locking or other techniques to prevent race conditions.  Optimistic locking relies on checking whether data has changed since it was last read. If so, the transaction is aborted and the client needs to retry.