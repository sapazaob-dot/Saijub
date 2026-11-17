# Saijub 30-second results tracker

A small Node.js + Express app with a 30-second cycle display, result history, historical counts, and an admin login to add/delete results.

## Run locally

1. Install Node.js 18 or newer.
2. In this folder run `npm install`.
3. Set environment variables (recommended):
   - `ADMIN_USER` (default: `saijub`)
   - `ADMIN_PASSWORD` (default: `ChangeMe123!` — change this before deployment)
   - `SESSION_SECRET` (a long random secret)
4. Run `npm start` and open `http://localhost:3000`.

## Deploy

Deploy as a Node web service on Render, Railway, or another Node host. Set the environment variables above. Attach persistent storage for `data.json` or replace the JSON storage with a database for production/multiple instances. Do not deploy with the default password.

## Notes

- The timer is a display based on 30-second Unix-time intervals; configure the period format to match your actual provider if needed.
- Results are entered manually by an admin. This app does not connect to or scrape any betting platform.
- Historical counts are descriptive only. They do not predict or guarantee future random outcomes.
- For production use, add a database, rate limiting, CSRF protection, HTTPS, backups, and stronger session management.
