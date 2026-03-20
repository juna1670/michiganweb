# Idobata Next.js Community Site

## Added in this version

1. Image upload (up to 4 images per post)
2. Post edit / delete
3. Admin approval workflow

## Tech stack

- Next.js 15
- TypeScript
- SQLite (better-sqlite3)
- Cookie session auth
- File upload to `public/uploads`

## Main behavior

- Public users can only see `approved` posts.
- New posts are created as `pending`.
- Edited posts return to `pending`.
- Admin can approve or reject in `/admin`.
- Authors can edit or delete their own posts.

## Demo accounts

| Role | Email | Password |
|---|---|---|
| Admin | admin@example.com | demo1234 |
| Member | demo@example.com | demo1234 |

## Setup

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:3000
```

## Main routes

| Route | Purpose |
|---|---|
| `/` | Home / search / approved posts only |
| `/register` | Sign up |
| `/login` | Login |
| `/dashboard` | My posts |
| `/posts/new` | New post |
| `/posts/[id]` | Post detail |
| `/posts/[id]/edit` | Edit post |
| `/admin` | Admin approval page |

## Notes

- Uploaded files are stored in `public/uploads`.
- Database file is stored in `data/idobata.db`.
- In this environment, `npm install` may fail because external package download can be blocked, but the source code structure is ready for local development.
