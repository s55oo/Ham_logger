# Ham_logger
Simple radio amateur logger

## Data storage

This is a single-file, offline-first app (`hamradio_logger.html`) — everything is kept in your browser, scoped to wherever you open the file from. Nothing is sent to a server.

| What | Where | Key |
|---|---|---|
| Logged QSOs | `localStorage` | `hamlog_entries_v1` (JSON array of all logged contacts) |
| Your callsign ("my call" field) | `localStorage` | `hamlog_mycall_v1` |
| Connected ADIF file handle (for auto-save/reconnect) | `IndexedDB` | database `hamlogger-db`, store `handles`, key `adifFile` |

Use **Export ADIF** any time to get a portable `.adi` copy of your log — this is the recommended way to back up or move your QSOs, since the browser storage above is local to one browser/profile and can be cleared by the browser.
