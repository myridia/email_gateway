# AGENTS.md — email_gateway

## What this is
Email Gateway API server for processing emails sent from static/ajax websites. Useful for handling contact forms.

## Stack
- Rust (edition 2024)
- Axum (web framework)
- lettre (email sending)
- tokio (async runtime)
- JWT / HMAC (auth)

## Build
```bash
cargo build --release
```

## Run
```bash
cargo run
```
Service managed via systemd on Debian: `systemctl status email_gateway`

## Structure
- `src/main.rs` — entry point
- `src/lib.rs` — library root
- `src/email.rs` — email processing
- `src/token.rs` — JWT token handling
- `src/nslookup.rs` — DNS lookup
- `src/test.rs` — tests

## Conventions
- No comments in code unless asked.
- Verify: `cargo check && cargo build`
