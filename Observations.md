# Database-Level Validation — Observations

## 1. Missing Task Title
The database rejected the insertion because the task title was NULL. This confirms that the `NOT NULL` constraint on `tasks.title` works correctly.

## 2. Duplicate Email
The database rejected the insertion because the email address already existed. This confirms that the `UNIQUE` constraint on `users.email` works correctly.

## 3. Invalid Priority
The database rejected a task with priority 10. This confirms that the `CHECK` constraint restricts task priority to values between 1 and 5.

## 4. Invalid Project Reference
The database rejected a task referencing project ID 999 because that project does not exist. This confirms that the foreign key constraint works correctly.

## Conclusion
All four invalid insertions were rejected by the database constraints, confirming that the required database-level validations work as expected.