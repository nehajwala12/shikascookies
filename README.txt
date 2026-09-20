SHIKA'S — M&M GOURMET COOKIES
Static site. No build step, no dependencies.

------------------------------------------------------------------
DEPLOY TO VERCEL
------------------------------------------------------------------
Easiest (no account setup beyond signing in):
  1. Unzip this folder.
  2. Go to vercel.com/new
  3. Drag the unzipped FOLDER onto the page (not the .zip).
  4. Deploy. You get a live URL in a few seconds.

Framework preset: "Other". There is no build command and no
output directory to set — it is plain HTML.

From the command line instead:
  npm i -g vercel
  cd <this folder>
  vercel

------------------------------------------------------------------
CUSTOM DOMAIN
------------------------------------------------------------------
Vercel project -> Settings -> Domains -> add shikascookies.com
(or whatever you buy) and follow the DNS instructions.

------------------------------------------------------------------
TWO THINGS TO UPDATE AFTER YOU HAVE A DOMAIN
------------------------------------------------------------------
1. In index.html, the four og:image / twitter:image tags near the
   top use a RELATIVE path. Link previews (iMessage, Instagram
   bio, WhatsApp) need an ABSOLUTE one. Change:
        content="assets/d_hero.jpg"
   to:
        content="https://YOURDOMAIN.com/assets/d_hero.jpg"

2. The TikTok and Instagram links in the footer currently point
   to "#". Search index.html for  <a href="#">TikTok</a>  and drop
   the real profile URLs in.

------------------------------------------------------------------
STILL PLACEHOLDER
------------------------------------------------------------------
- "Est. 2025" in the hero
- Collection point: "Upper East Side"
- Delivery fees: $12 Manhattan / $18 Brooklyn
- The example order details (Maya R. etc.) are intentional — they
  show a visitor what a filled-in slip looks like.

------------------------------------------------------------------
HOW THE ORDER FORM WORKS
------------------------------------------------------------------
There is no server. The form builds an order slip in the browser,
then "Copy the slip" or "Send by email" hands it to the customer's
own mail app, addressed to nehaissooawesome@gmail.com. Nothing is
stored anywhere. If you later want orders to land in a database or
a spreadsheet automatically, that needs a form service — say the
word and it is a small change.

Files: index.html + assets/ (8 photos, 2 icons). Nothing else needed.
