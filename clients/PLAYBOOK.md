# Client playbook

What worked with Don Bowman, written down so it can be repeated.

## The offer (same for every client)
- $300 one-time: redesign + move, paid only when the new site is live and approved.
- $10/month: hosting, domain renewal, fixes. Cancel any time.
- Changes: $25 each, 3 for $60, 5 for $90. Bigger work quoted first.
- They own the domain and content. Leaving is free and you help them move.

## Who to look for
A good lead has all three:
1. **A small local business with an owner you can talk to directly.** Massage therapists, barbers, cleaners, trainers, tutors, handymen, small restaurants.
2. **A site that's old, broken, or on a platform they can't use.** Signs: "Control Panel" or "Powered by" in the footer, missing photos, dead links, not mobile-friendly, a Facebook page as the "website".
3. **They already pay for something.** Many pay $20–50/month for a builder they never touch.

### Best niche to start: massage therapists on AMTA/BodyworkSites
- Same setup as Don. AMTA members get BodyworkSites at $19.95 or $49.95/month, month to month
  ([BodyworkSites AMTA pricing](https://www.amtamembers.com/pricing)).
- These sites all look alike and are easy to spot: page source contains `/amta/sites/css` or a
  "Control Panel" link in the footer.
- Find them: [AMTA Find a Massage Therapist](https://www.amtamassage.org/find-massage-therapist/),
  search Lansing / East Lansing / Okemos / Holt / DeWitt, open each therapist's website.
- Pitch line: "You're paying about $50 a month for a site you have to edit yourself. I can host
  it for $10 a month, and when you need a change you just call or text me. Changes are $25 each,
  cheaper in batches."

### Lyft passengers
- When someone mentions they run a business, ask for the website name. Look at it after the ride.
- Only follow up if it clearly has problems (see signs above). Don't pitch in the car.

## The steps (about 2 hours of your time per client)
1. **Find** the lead and note the site address.
2. **Demo (under 1 hour):** rebuild their home page from their real content and photos. Copy the
   folder `clients/donald-bowman/site` as the starting template.
3. **Send a short message:** "I noticed your site [one specific problem]. I made a quick version
   of what it could look like: [link]. Happy to talk if you're interested." One follow-up after a
   week, then drop it.
4. **When they reply with feedback, make the fixes and send the offer** (copy
   `clients/donald-bowman/OFFER-MESSAGE.txt`, change the details).
5. **Deliver** using the switch-over order in `clients/donald-bowman/README.md`: preview first,
   domain control, DNS with email records copied, test, then they cancel the old service.

## Rules
- Real content only. Never invent reviews, prices, hours or credentials. Ask.
- One new demo at a time. Don't build 10 demos nobody asked for.
- Keep it boring: static sites, no databases, no logins.
- Goal: 5 clients = $50/month recurring + $1,500 in setup fees. That covers your subscriptions.

## Tracker
| Business | Contact | Site | Problem spotted | Demo sent | Replied | Offer sent | Status |
|---|---|---|---|---|---|---|---|
| Donald Bowman Massage | (517) 927-3883 | blindmassage.com | Can't edit BodyworkSites, photos/video missing | yes | yes | yes | Accepted, transfer in progress |
| Lansing Upholstering Service & Interior Accents | (517) 485-8950 | interioraccentslansing.com | Dated Thryv site, stock photo instead of their own work, Yahoo email | no | | | Lead |
| Our Shop Upholstery | ourshopupholstery@outlook.com | Facebook only | No website, "message us on Facebook" | no | | | Lead |

### Scan notes (2026-09-28)
Checked ~30 Lansing small-business sites. Most were fine (Wix, Squarespace, Duda, agency WordPress):
Frandor Tailor, Low Cost Auto, Randall Auto, Lake Lansing Rd Mobil, Holt Auto, Lansing Chiropractic,
Silver Platter Cleaning, Keast Lawn, Four Seasons Lawn, Quality Tire, Tooth & Nail Grooming,
Gall Sewing (gallsewingvac.com), Muffler Man, Richardson Music Studio (old Weebly, but works on phones).
Lesson: "bad website" is rarer than expected. Better targets are businesses with **no website**
(Facebook-only or Google listing only) and owners stuck on platforms they can't edit.
