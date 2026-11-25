# Business Profile Registration

Register one business across directories and profile sites to build an entity / backlink footprint, at scale (target can be 100+ profiles). Field-proven end-to-end on Diamond Rise (100 profiles, Nov 2026).

Owner-facing guide: `HUONG-DAN-SU-DUNG.md` (in this folder) — how the owner runs this skill on Muse: what to prepare, sample commands, what Muse does, the owner-only batch, and the limits. Point the owner to it when they ask how to use the skill.

Reference files in this skill:
- `references/platform-pool.md` — the reusable candidate pool: every platform tried, grouped by outcome (works / verify-first / do-not-retry with the reason). Start every new business from this pool instead of researching from scratch.
- `references/diamond-rise-100-profiles.md` — the finished Diamond Rise master list (100 profiles with live URLs and status notes), as the worked example of the output format.
- `references/untried-candidates-manh-digital.md` — 283 UNTRIED candidate platforms imported 2026-11-25 from the Mạnh Digital "Social Entity" sheet (414 platforms; the other ~131 already appear in the pool or the Diamond Rise list). AS scores and link types there are the sheet author's claims, not field-verified — work them as verify-first candidates and promote each into the pool's WORKS / DO-NOT-RETRY sections only after an actual attempt.

## Phase 0 — Lock the identity once

Collect before registering anywhere; never start with gaps:

- **First deliverable of every run: generate the brand info sheet.** Before registering anywhere, produce an XLSX modeled on the "Mẫu thông tin hồ sơ" tab of the Mạnh Digital Social Entity sheet (adopted 2026-11-25), pre-filled with the locked identity below: columns `Mục | Thông tin | Số ký tự (live =LEN formula) | Tối đa | Gợi ý`, in four sections — (1) basic info (brand name, legal name, address, phone, contact email, website, country/city, founding year, industry, tax ID, hours); (2) bios in the four length tiers (micro 80 / short 150 / medium 300 / long 1,000) in VN + EN, plus 2–3 target keywords; (3) preferred username + fallbacks (≤15 chars), the registration email, avatar (square logo ≥400×400) and cover (~1500×500) specs; (4) the 2–3 strongest existing profiles for cross-linking. Name it `Mau-Thong-Tin-Ho-So-<Brand>.xlsx` and save it next to the master list. Every registration then copies verbatim from this sheet — it is the single source of truth for the whole run. The workbook has a second sheet, `Profile & Thông tin hồ sơ`, with exactly TWO columns: column A **Profile** — one row per profile (number, platform, public URL or the no-URL note, short status), kept in sync with the master list as profiles are added; column B **Thông tin hồ sơ** — the locked identity as one "field: value" line per row (including which bio tier to use where), so a registration session can read profiles and the exact info to paste side by side without opening anything else. Worked example: `~/workspace/your_files/backlink-diamond-rise/Mau-Thong-Tin-Ho-So-Diamond-Rise.xlsx`.

- Registered legal name, copied exactly from the business registration (never a shortened brand/NAP variant — directories that check documents will reject or split the entity).

- Founding year from the registration document (never a website milestone or brand story).

- Tax ID, HQ + branch addresses in the current administrative format, public email, hotline, opening hours, slogan, service list, customer count only if the business itself publishes it.

- Standard bios written once in VN + EN and reused verbatim everywhere — prepared in FOUR length tiers so any platform's cap is covered without editing on the spot: micro ≈80 chars (TikTok / slogan fields), short ≈150 chars (most bio fields; fits X 160 and Instagram 150), medium ≈300 chars (forum About fields), long ≈1,000 chars (company pages, YouTube, LinkedIn, directories — main services, service area, contact). Count characters when drafting each tier. (Tier structure adopted 2026-11-25 from the "Mẫu thông tin hồ sơ" tab of the Mạnh Digital Social Entity sheet; field experience agrees — Peerlist caps at 120, HeyLink 50, CodePen 100, HackMD 160, Note 140, Luma ~144.)

- Logo file (square PNG) and brochure PDF if the business has one.

- Preferred username + two fallbacks; an account-holder convention for forms that demand a person (e.g. First "Diamond", Last "Rise", title "Owner"); the owner's date of birth if platforms demand one (ask once, remember it, never substitute the founding date).

- One designated account (the company Gmail) for ALL registrations. Never write its password into files or memory; fetch verification codes and magic links from that mailbox in the browser yourself.

## Phase 1 — Harvest what already exists (free wins first)

Before creating anything, check for pre-existing presence and count what verifies:

- Official social channels (Facebook, Instagram, TikTok, X, YouTube, Threads, LinkedIn profiles).

- Auto-generated data records (tax/business registries, Opencorporates, D&B, Cybo and local equivalents) — verify the data; flag wrong legal-rep / tax-ID contamination to the owner, but do not contact third parties about it unprompted.

- Map listings (Google Business Profile, Bing Places, Apple Maps, HERE, Waze, TomTom) and older accounts from previous attempts.

- Update editable stale profiles to the locked standard; never force a duplicate.

## Phase 2 — Registration waves

- Run parallel browser sessions with **at most 2 sites per session**. Field lesson: 3–4-site sessions repeatedly died mid-run; 2-site sessions finished reliably. Use single-site sessions for stubborn platforms.

- Order: high-value directories first (Google Business, Crunchbase, Clutch-type), then publishing/profile sites, then link pages, then the creator/dev/audio long tail from the pool.

- Pace the waves across days: spread registrations out (a modest batch per day) instead of creating hundreds of profiles in one burst — it looks natural to platforms, lowers bulk-registration lock risk, and avoids draining rate limits in a single day. (Adopted 2026-11-25 from the Mạnh Digital sheet's Grok Bot tab, step 10.)

- Time-box about 5 minutes per step. Credential waits (a secure-entry card) cap at **4 minutes**, then skip that site and move on.

- Save every verified URL in ONE master list the moment it verifies; keep a per-wave tracker for in-flight candidates. Report progress leading with the running TOTAL count, and batch-report parked/skipped sites at the end instead of interrupting the owner per site.

## Sign-in decision tree (apply per site, with one exception)

The one exception is the owner-ordered single batch sitting in Saved passwords do not move to new signups.

1. Google SSO offered → sign in with the company Google account; fetch any code/link from the company mailbox yourself.
2. Google SSO works but the site then demands its own new password (Viblo, Strikingly pattern) → PARK, unless the owner has ordered reuse of the same old company password and agreed to one batch sitting. Reusing that same old password is not creating a new per-site password. Never create a new per-site password and never run a secure-entry-card campaign at the owner outside that agreed sitting.
3. Email + password only, no Google → PARK the same way, with the same sole exception.
4. Mandatory phone/SMS verification with no skip (Beehiiv pattern), ID upload, or employer phone-OTP / business-license upload → PARK as owner-only. Never use a personal number unprompted. If the owner has ordered stuck groups cancelled, drop them entirely and replace them with fresh candidates from the pool.
5. Bot walls: press-and-hold checks (PerimeterX) and most Turnstile checks yield to the browser's bot specialist — let it work. Looping Cloudflare checks that keep resetting tokens, DataDome hard blocks, and country blocks → PARK and retry later from another network/time.
6. A sign-in fails once → exit that platform and do the next one. No retry loops inside a session.

## Saved passwords do not move to new signups

- Use the same old company password for a new signup when the owner has ordered it, instead of inventing a new password for that site.

- Remember that the vault cannot copy a saved password onto a brand new signup form, so the owner must type that password once into the card for each new site, and the vault saves it for that site only after that first entry.

- Never tell the owner that a saved password has been applied to a waiting session until that session actually moves past its card, and report only what the session shows.

- Do not open password card sites one by one across separate sessions, collect the waiting cards into one list and reopen them together in one sitting only when the owner has agreed to that sitting, so the owner enters each card once and the work moves on. This batch sitting is the sole exception to steps 2 and 3 of the sign-in decision tree.

- Never ask the owner to share a password value in chat, and never claim to have entered a password on the owners behalf, because Muse never sees the password value.

- Unlike Grok Bot (whose vault is built into its own browser and auto-generates a fresh password per site), Muse's Secure Vault cannot auto-generate or inject a password into a new signup: the owner sets/types the password on the secure-entry card — either the same reused company password (the owner's standing rule) or a different one per site if the owner chooses to type different values during the batch sitting. Do not generate passwords in chat.

## Verify everything — sessions die silently

- A profile counts ONLY when its public URL opens (logged-out view) and shows the locked name, bio and logo. Verify it yourself before adding it to the master list.

- While verifying, record whether the profile's website link is dofollow or nofollow: inspect the link on the public page (browser Inspect → the anchor's `rel` attribute; no `rel="nofollow"` means dofollow). Note it in the master list next to the URL. (Adopted 2026-11-25 from the Mạnh Digital sheet's Grok Bot tab, step 9.)

- Browser sessions often die without a report AFTER finishing the work (recovered this way in the field: Spreaker, 500px, Webflow, HackMD, Wattpad). When a session dies: (a) list the browser windows — surviving tabs reveal the profile URLs; (b) fetch the suspected public URLs directly and check their content; (c) relaunch only what is actually missing, framed as a "verify and finish" task.

- Distinguish states in the tracker: live / submitted-pending-review / pre-existing-unclaimed / created-but-unpublished. Never report a pending-review URL as live.

## Fill rules

- Never invent data: no made-up rates, prices, founding years or client counts. Use only locked values; leave optional fields blank.

- Adapt to platform limits without asking: bio character caps (HackMD 160, Luma ~144, CodePen 100 — shorten while keeping name, services, hotline), bios that ban contact info (Dribbble), free plans with no website field (put the URL in the bio text), platform-assigned usernames that cannot change (LeetCode), taken usernames (use the fallbacks). Note each quirk in the tracker.

- Free plans only: never enter payment details; never connect payout methods (Ko-fi, Buy Me a Coffee, Gumroad, Streamlabs tips stay unconnected); decline auto-renewing trials and pick the true free tier (e.g. Ucraft's Website plan, not the Shop trial); never pay a claim fee (e.g. Foursquare $20) without the owner's explicit say-so.

- Content restraint: profile shells only — no posts, articles, events, job listings or gigs unless the owner asked. A first intro article needs the owner's approval before it is published anywhere. Publishing the owner's own brochure as flipbooks (Scribd, Calameo, Flipsnack, FlipHTML5) is the standing exception.

## Phase 3 — Cross-linking

- Pick one link hub (About.me) that lists ALL profiles. Every profile links to the main website; profiles with room also link siblings; one-link platforms point to the hub.

- Add cross-links during creation whenever the field exists, to avoid a second pass.

## Phase 4 — Force indexing (ép index)

Reality first: profiles live on third-party domains, so they cannot be submitted in Google Search Console or Bing Webmaster Tools (those only accept properties you own). "Forcing" indexing means making crawlers discover the profiles fast through pages they already crawl:

1. **Build directory pages with the FULL profile list.** On crawl-friendly properties created in Phase 2, publish one page titled "Hồ sơ chính thức của <Business> trên các nền tảng" containing every profile URL as a CLICKABLE link (label + linked URL), plus an intro line with the legal name, main website and hotline. Field-proven set: a WordPress.com static Page, a Blogger static Page, a section appended to the public Notion page, and a links section on the Google Sites page. The About.me hub from Phase 3 serves the same role for humans.
2. **Ping the update services.** After publishing the WordPress and Blogger pages, submit each blog to Ping-O-Matic (pingomatic.com): blog name, blog home page URL, and its RSS feed URL (WordPress: /feed/; Blogger: /feeds/posts/default), check all common services, send. A "Ping sent" result notifies aggregators that pull Google/Bing crawlers in.
3. **Let the link graph do the rest.** Directory pages link OUT to every profile; profiles link to the website + hub (Phase 3). One crawl of a directory page fans out to the whole footprint.
4. **Verify and set expectations.** Open each directory page logged-out, spot-check several hrefs (especially long/easily-mangled URLs), and record the directory page URLs in the master list. Indexing then takes days to weeks — never promise instant index; spot-check later with `site:<platform-domain> <brand>` searches.

Worked example (Diamond Rise, 12/11/2026): WordPress page with 94 links + Ping-O-Matic ping, Blogger page with 70 links + ping, Notion section with 68 link lines, Google Sites section with 7 key links + hub.

## Owner-only batch (collect silently, hand over once)

Claim and verification steps only the owner can finish — Google Business ownership transfer, Bing PIN verification, Trustpilot activation through the domain email, Apple ID claim, LinkedIn Company Page (needs a personal admin), Zalo OA, employer license uploads — go into ONE batch list handed to the owner at the end, not one interruption per site.

## Available connectors

- Use muse.connector_search to find other connectors and muse.skill_search to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with Custom Connectors and MCPs, or build a custom connector.
