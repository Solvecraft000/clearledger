# Invoice creation idempotency

Authenticated invoice creation accepts an idempotency key scoped to the
requesting account. Repeating the same key returns the persisted transaction
mapping without creating a second invoice; conflicting payloads for a reused
key are rejected for operator visibility.
