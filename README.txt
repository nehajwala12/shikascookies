SHIKA'S - M&M GOURMET COOKIES
Static site. No build step, no dependencies.

==================================================================
STEP 1 - TURN ON EMAIL (DO THIS FIRST, TAKES ~30 SECONDS)
==================================================================
Right now the order form falls back to opening the visitor's own
email app. To make it send straight to your inbox instead:

  1. Go to  https://web3forms.com
  2. Type in  nehaissooawesome@gmail.com  and submit.
     (No account, no password, no credit card.)
  3. An access key arrives in your inbox immediately.
     It looks like:  a1b2c3d4-e5f6-7890-abcd-ef1234567890
  4. Open index.html in any text editor. Near the bottom, find:

         var WEB3FORMS_KEY  = "REPLACE_WITH_YOUR_ACCESS_KEY";

     Paste your key between the quotes:

         var WEB3FORMS_KEY  = "a1b2c3d4-e5f6-7890-abcd-ef1234567890";

  5. Save. Done - both the order form and "The List" signup now
     email you directly.

What you receive per order: the sizes, the total, the customer's
name and contact, collection/delivery, the date needed, their
notes, and the full slip. If the customer gave an email address,
hitting Reply goes straight back to them.

The free tier covers 250 submissions a month.

A hidden anti-spam field is already wired in - bots that fill it
are silently dropped.

==================================================================
STEP 2 - DEPLOY TO VERCEL
==================================================================
  1. Unzip this folder.
  2. Go to  vercel.com/new
  3. Drag the unzipped FOLDER onto the page (not the .zip).
  4. Deploy.

Framework preset: "Other". No build command, no output directory.

From the command line instead:
  npm i -g vercel
  cd <this folder>
  vercel

CUSTOM DOMAIN: Vercel project -> Settings -> Domains.

==================================================================
STEP 3 - ONCE YOU HAVE A DOMAIN
==================================================================
The og:image / twitter:image tags near the top of index.html use a
RELATIVE path. Link previews (iMessage, Instagram bio, WhatsApp)
need an ABSOLUTE one. Change:
      content="assets/d_hero.jpg"
to:
      content="https://YOURDOMAIN.com/assets/d_hero.jpg"

==================================================================
STILL PLACEHOLDER
==================================================================
- TikTok and Instagram links in the footer point to "#"
- "Est. 2025" in the hero
- Collection point: "Upper East Side"
- Delivery fees: $12 Manhattan / $18 Brooklyn
- The example order details (Maya R. etc.) are intentional - they
  show a visitor what a filled-in slip looks like.

==================================================================
A NOTE ON THE TESTIMONIALS
==================================================================
The Praise section carries TWO quotes, both real, taken from the
texts you sent. A third was invented as placeholder and has been
removed - made-up reviews on a site that takes real money are a
genuine liability, so they should only go back in as real ones.
Send any real texts and they can be added.

Files: index.html + assets/ (8 photos, 2 icons). Nothing else.
