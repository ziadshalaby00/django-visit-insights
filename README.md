# django-visit-insights

**Track your Django site's visits without slowing it down.**

Most visit-tracking libraries either hit the database on every request (slow under load) or force you to install Celery, Redis, and a background worker just to count clicks (heavy for a simple counter). `django-visit-insights` takes a simpler path: every visit increments a fast counter in your cache — Redis, Memcached, or anything Django supports — and a single management command runs periodically (via cron) to move those numbers into the database in one batch. Your hot path stays fast, your database stays quiet, and you don't need a single extra dependency beyond Django itself.

For admins, the library ships with a clean dashboard at `/insights/` showing total visits, today's count, hourly trends, and top pages — all updating live in the browser thanks to Server-Sent Events, so you can literally watch the numbers move as people browse your site. No polling, no refresh button, no WebSocket setup. Just an open connection and a stream of updates.

Developers who want the numbers elsewhere get a small JSON API (`/insights/api/stats/`) and a live event stream (`/insights/api/stream/`) they can plug into any frontend. Want to show today's visits in your navbar? Two lines of JavaScript. Want to log them into your own analytics pipeline? One HTTP call.

That's the whole idea: **count fast in cache, persist in batches, show it live** — and let you get out of the way.

---

**Install:** `pip install django-visit-insights`
**Setup:** add the app, add the middleware, schedule one cron job. Done.

MIT License.
