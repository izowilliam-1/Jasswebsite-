# JASS Website — Admin Login Setup Guide

This site includes a real content-editing system: staff can log in at `/admin/`
and edit the Contact page, News, and Staff directory, with changes saved
directly to the live site. This only works once you complete the steps below —
it does **not** work by just opening the HTML files locally.

This setup is free and takes about 15–20 minutes.

---

## 1. Put the site on GitHub

1. Create a free GitHub account if you don't have one: https://github.com/signup
2. Create a new repository (e.g. `jass-website`)
3. Upload all the files in this folder to that repository — including the
   hidden-looking `admin/` and `_data/` folders. (You can drag-and-drop files
   on github.com, or use `git push` if you're comfortable with Git.)

## 2. Connect it to Netlify

1. Create a free Netlify account: https://app.netlify.com/signup (sign up with
   your GitHub account — it's easiest)
2. Click **Add new site → Import an existing project**
3. Choose **GitHub**, then select your `jass-website` repository
4. Leave the build settings empty (this is a static site, no build step needed)
   and click **Deploy**
5. Netlify gives you a live URL like `https://random-name-123.netlify.app` —
   you can rename this later, or connect a real domain (e.g. `jass.school`)
   under **Site settings → Domain management**

## 3. Turn on Netlify Identity (this is the real login system)

1. In your Netlify site dashboard, go to **Site configuration → Identity**
2. Click **Enable Identity**
3. Under **Registration preferences**, choose **Invite only** — this means
   nobody can sign themselves up; only people you personally invite can log in
4. Scroll to **Services → Git Gateway** and click **Enable Git Gateway** —
   this is what lets logged-in staff actually save changes back to the site

## 4. Invite staff who should be able to edit the site

1. Still under **Identity**, click **Invite users**
2. Enter the email address of each staff member who should have access
   (e.g. the Principal, a designated office staff member)
3. They'll receive a real email invite. Clicking it lets them set their own
   password — you never see or choose their password
4. They can then go to `yoursite.netlify.app/portal.html` and click
   **Open Content Manager** to log in and edit content

## 5. Test it

1. Visit `yoursite.netlify.app/admin/`
2. Log in with an invited account
3. Try editing the Contact Info — phone, email, address, banks, office hours
4. Save — this creates a real commit to your GitHub repository and updates
   the live Contact page within a minute or two

---

## What staff can edit

- **Contact Info** — address, phone numbers, email, office hours, payment bank names
- **News & Notices** — add/edit school announcements
- **Staff Directory** — add/edit staff names and roles

## What this does *not* include (by design)

This system intentionally does **not** include student records, grades,
attendance, or fee/payment account numbers. Those involve real student data
and financial risk and need a properly designed, separately secured system —
not something bolted onto a content editor for a public website. If you need
that down the line, it's worth budgeting for a developer to build it properly
with a real database and access controls suited to handling student data.

## Costs

Everything above is free at this scale: Netlify's free tier, Netlify Identity's
free tier (up to 5 active users), and GitHub's free tier all comfortably cover
a small school site. You only start paying if traffic or user counts grow far
beyond what a school site like this typically sees.
