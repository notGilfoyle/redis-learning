E# M3 — Expiry, Persistence & Keyspace

## What I learned
- TTL with EX/PX, EXPIRE, TTL, PERSIST
- RDB = periodic snapshots, AOF = every-write log
- Keyspace notifications = event-driven reactions to key changes

## Project
OTP + Session Store — real-world TTL use cases

## Key patterns
- SET key value EX seconds → atomic set + expiry
- DEL after verify → one-time use keys
- EXPIRE reset on activity → sliding session expiry
- PSUBSCRIBE __keyevent@0__:expired → react to expiry events