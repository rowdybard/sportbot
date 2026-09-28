# blindmassage.com rebuild (Donald Bowman)

Static site for Donald Bowman's massage practice. It replaces the AMTA/Bodyworksites site
at www.blindmassage.com, with Don's requested changes:

- Photos from his current site are back (portrait + at-work photo), with descriptive alt text.
- "Studio Tour 2022" YouTube video is embedded, plus a plain link to it.
- Wording: "Donald is a massage therapist who happens to be blind."
- Intake form removed. "Your first visit" explains the 90-minute first session that starts
  with a sit-down interview.

Kept from the old site: services and prices, hours, reviews, Square Appointments booking (Don's top
priority, linked in the header and throughout), phone, email, address. PayPal removed at Don's
request; Venmo and Square payment links replace it. Old page URLs redirect to the matching section (`_redirects`).

## Preview locally

    npx wrangler pages dev site

## Deploy (Cloudflare Pages)

    npx wrangler pages deploy site --project-name blindmassage

Then in Cloudflare: Pages > blindmassage > Custom domains > add www.blindmassage.com and
blindmassage.com. Do this only after Don confirms who controls the domain, and don't let him
cancel the old site until the new one is live and booking, PayPal, and email are tested.

## Before going live

- Open https://venmo.com/u/BOWMAN16 and confirm it is Don's profile before going live.
- Hours confirmed by Don: Monday to Thursday 10 am to 10 pm, closed Friday to Sunday.
- Payments confirmed by Don: Square (booking app, invoices, card in person) and Venmo. No PayPal.
- Domain: Don never had a GoDaddy account. BodyworkSites registered it for him, so it is in
  their reseller account. Don must request the transfer authorization code from them (see
  `BODYWORKSITES-REQUEST.txt`).

## Domain and email facts (checked 2026-09-28)

- blindmassage.com is registered at GoDaddy since 2010, paid through 2027-04-13, transfer-locked
  (normal). Owner details are private, so first find out whose GoDaddy account it is in.
- DNS is run by BodyworkSites' provider (nameservers ns4/5/6.xvdns.com). The site points to 68.183.248.74.
- **Email is Google Workspace, not BodyworkSites.** When DNS moves, copy these exactly or his email breaks:
  - MX: 1 aspmx.l.google.com, 5 alt1.aspmx.l.google.com, 5 alt2.aspmx.l.google.com,
    10 alt3.aspmx.l.google.com, 10 alt4.aspmx.l.google.com
  - TXT: `v=spf1 include:_spf.google.com ~all`
  - Also check for any other records (e.g. Google site verification, DKIM `google._domainkey`) before switching.

## Switch-over order

1. Deploy to a Pages preview URL. Don (or someone he trusts) checks it with his screen reader.
2. Get control of the domain (Don's GoDaddy login, or BodyworkSites releases it to him).
3. Move DNS to Cloudflare with the email records above, then point the site at Pages.
4. Test: site loads, Book online opens Square, payment links work, send and receive a test email.
5. Only then Don cancels BodyworkSites.

## Deal and message

- `AGREEMENT.md`: the terms ($300 one-time, $10/month, $25 per change with batch pricing).
- `OFFER-MESSAGE.txt`: plain-text message to send Don. Plain text on purpose, so it reads cleanly on his screen reader.
