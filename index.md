# DuoBoard — Privacy Policy

*Effective date: June 28, 2026*

DuoBoard ("the app") is a kanban chore board for couples, published by Hamdi
Ghorbel. We built it to be as private as a notes app.

## The short version

- No ads, no analytics, no trackers, no selling of data. Ever.
- Your chores live in a local database on your phone. Android automatic backup
  and device-transfer backup are disabled for DuoBoard data.
- If — and only if — you turn on couple sync, your board is stored
  **end-to-end encrypted** on the self-hosted sync server so your partner's
  phone can receive it. We cannot read it. The server operator cannot read it.
   Only devices given the pairing code hold the decryption key. Anyone with
   that code can join, so share it privately; the service permits up to ten
   registered devices for a couple.

## Data stored on your device

Chores (titles, notes, dates, points), shopping lists, weekly check-ins,
partner display names and colors, and app settings are stored in a local
database. They never leave your device unless you enable sync or use the manual
export feature. The pairing key is encrypted with a non-exportable Android
Keystore key.

If you enable the **system calendar overlay** (Settings → Appearance &amp; behavior → Show
system calendar events), the app reads event titles, times, locations, and
descriptions from your phone's calendar (via `CalendarContract`) to display
them alongside chores in the calendar view. Calendar data is read-only — the
app never writes to or modifies your calendar. Calendar events are not uploaded
or synced to the DuoBoard server; they stay on your device.

## Data processed if you enable couple sync (optional)

When you create or join a couple:

- **What is uploaded:** chores, pinned notes, chore comments, tags, lists,
  weekly check-ins and their optional notes, board configuration, and display
  profiles are encrypted on your phone with
  AES-256-GCM before upload. The pairing key is generated on your phone and
  shared only inside the pairing code you exchange privately with your partner.
  The server stores ciphertext plus last-modified timestamps and opaque record
  identifiers.
- **Photos (if you attach one):** the image is downsampled and recompressed
  to ≤200 KiB on your phone, then encrypted with the **same** AES-256-GCM key
  and uploaded to the sync server as an opaque ciphertext blob. The server
  only stores ciphertext; it never sees the photo. Your partner's phone
  downloads and decrypts it on demand. The server caps each couple at
  20 photos / 10 MiB and rate-limits uploads.
- **Where:** the self-hosted DuoBoard sync server.
  No Google/Firebase storage is used for sync data. Only *background push
  notifications* transit Firebase Cloud Messaging so a closed app can be
  woken instantly. A push may carry encrypted event ciphertext; Firebase and
   the server cannot read it. FCM registration tokens and normal network
   metadata are processed to deliver these notifications. The sync server keeps
   a token until it is replaced, unregistered, or has not refreshed for 90 days.
- **Account:** none. The couple id is a random 128-bit value generated on your
  phone and carried only inside the pairing code. No name, email, or phone
  number is requested or stored.
- **Service data:** like any internet service, the server and its hosting
  provider transiently process IP addresses and basic request metadata to
  operate.

## Voice input

Voice input is available only on Android 12 or later when an on-device speech
recognizer is installed. DuoBoard does not fall back to a cloud recognizer, so
voice audio and transcripts stay on your phone.

## Data deletion

- **Leave couple** disconnects this phone, removes its FCM registration, and
  keeps this phone's local board.
- **Delete shared cloud copy** in Settings → Sync erases the encrypted server
  copy, removes registered devices, and disconnects both phones. Each phone
  keeps its local board unless its owner deletes or uninstalls the app.
- Manual exports are user-managed files. They are not included in Android
  automatic backup and are not removed by DuoBoard.

## Children

DuoBoard is intended for adults managing a household together and is not
directed at children under 13.

## Changes

If this policy changes, the updated version will be published at the same
address with a new effective date.

## Contact

Hamdi Ghorbel — ghorbelhamdi@gmail.com
