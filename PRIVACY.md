# DuoBoard — Privacy Policy

*Effective date: June 26, 2026*

DuoBoard ("the app") is a kanban chore board for couples, published by Hamdi
Ghorbel. We built it to be as private as a notes app.

## The short version

- No ads, no analytics, no trackers, no selling of data. Ever.
- Your chores live in a local database on your phone.
- If — and only if — you turn on couple sync, your board is stored
  **end-to-end encrypted** on the self-hosted sync server so your partner's
  phone can receive it. We cannot read it. The server operator cannot read it.
  Only the two paired phones hold the decryption key.

## Data stored on your device

Chores (titles, notes, dates, points), partner display names and colors, and
app settings are stored in a local database. They never leave your device
unless you enable sync or use the manual export feature.

## Data processed if you enable couple sync (optional)

When you create or join a couple:

- **What is uploaded:** your chores and partner display names, encrypted on
  your phone with AES-256-GCM before upload. The encryption key is generated
  on your phone and shared only inside the pairing code you exchange
  privately with your partner. The server stores ciphertext plus a
  last-modified timestamp.
- **Where:** the self-hosted DuoBoard sync server. No Google/Firebase storage
  is used for sync data. Only *background push notifications* (a content-free
  wake-up ping, no chore data) transit Firebase Cloud Messaging so a closed
  app can be woken instantly.
- **Account:** none. The couple id is a random 128-bit value generated on
  your phone and carried only inside the pairing code. No name, email, or
  phone number is requested or stored.
- **Service data:** like any internet service, the server and its hosting
  provider transiently process IP addresses and basic request metadata to
  operate.

## Data deletion

- Turning off sync ("Leave couple") stops all uploads; uninstalling the app
  deletes the local database.
- To remove synced ciphertext from the server, contact us at the address
  below with your couple ID, or simply leave the couple on both phones — the
  data is unreadable without your key in any case.

## Children

DuoBoard is intended for adults managing a household together and is not
directed to children under 13.

## Changes

If this policy changes, the updated version will be published at the same
address with a new effective date.

## Contact

Hamdi Ghorbel — ghorbelhamdi@gmail.com
