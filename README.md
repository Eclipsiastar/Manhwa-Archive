# Manhwa Archive

A dark-themed manhwa catalogue and personal reading tracker. This repository contains the full single-page HTML app and its logo.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser. Some browser security settings may limit modules or network features when opened directly; if so, use a static host or a local HTTP server.

## Deploy

This is a static site. You can deploy the repository with Netlify or GitHub Pages. The entry file is `index.html` and the logo is in `manhwa-archive-logo.svg`.

## Supabase configuration and security

The app currently contains a Supabase project URL and a publishable/anon client key in `index.html`. Publishable/anon keys are intended for browser use, but **they are not a security boundary**. Before making the app public, verify that Row Level Security (RLS) is enabled and that every table has carefully scoped policies. Never put a Supabase `service_role` key, database password, OAuth client secret, or other private secret in this repository.

If you fork this project for your own use, replace the Supabase URL and publishable/anon key with your own project's values and apply your own schema and RLS policies. Do not assume the hosted backend is yours or that the demo is production-ready without testing authentication, catalogue submissions, moderation, storage, and integrations.

## Notes

- The main application is `index.html`.
- This package preserves the existing app source and changes the header mark to use the repository logo asset.
- Third-party integrations require their own valid configuration and may not be active until set up.
