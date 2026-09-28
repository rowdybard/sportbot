# blindmassage.com rebuild (Donald Bowman)

Static site for Donald Bowman's massage practice. It replaces the AMTA/Bodyworksites site
at www.blindmassage.com, with Don's requested changes:

- Photos from his current site are back (portrait + at-work photo), with descriptive alt text.
- "Studio Tour 2022" YouTube video is embedded, plus a plain link to it.
- Wording: "Donald is a massage therapist who happens to be blind."
- Intake form removed. "Your first visit" explains the 90-minute first session that starts
  with a sit-down interview.

Kept from the old site: services and prices, hours, reviews, Square booking link, PayPal payment
form, phone, email, address. Old page URLs redirect to the matching section (`_redirects`).

## Preview locally

    npx wrangler pages dev site

## Deploy (Cloudflare Pages)

    npx wrangler pages deploy site --project-name blindmassage

Then in Cloudflare: Pages > blindmassage > Custom domains > add www.blindmassage.com and
blindmassage.com. Do this only after Don confirms who controls the domain, and don't let him
cancel the old site until the new one is live and booking, PayPal, and email are tested.

## Before going live, confirm with Don

- Friday to Sunday hours (the old site only lists Monday to Thursday).
- Whether the email address still works and whether PayPal is still in use.
- Where his domain is registered. The domain's email (MX) records must be kept when DNS moves.
