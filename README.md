# cheap yearly vps: real annual costs from $7 promo boxes to €6.95/month KVM, the refund fine print nobody mentions, and how to pick without overpaying

Searching for a cheap yearly VPS usually means one of two things: you want a $10–30/year box for a side project, or you've been burned by a "cheap" host whose renewal price doubled and you want the real annual cost this time. Both questions have concrete answers, and the numbers are more spread out than the "cheapest VPS" listicles suggest.

The short version: the genuinely cheap yearly tier starts around $7–22/year for 1–2 GB KVM boxes from promo-driven hosts like RackNerd and DediRock. V.PS (the brand behind vps.hosting, operated by xTom OÜ in Estonia) sits in a different lane: KVM plans from €6.95/month, billed monthly in EUR, across 11 city locations — with every listed price doubling as the renewal price, and a 14-day refund window on VPS orders. Which lane fits depends on what "cheap" means to you: the lowest possible invoice, or predictable cost with an exit ramp.

> **Quick take**
> - Lowest yearly bill, no refund expectations: the promo tier — RackNerd from $21.99/year standard (seasonal drops to $11.29/year), DediRock's Promo Saver at $8.88/year.
> - KVM, 99.9% SLA, guaranteed bandwidth, 11 cities, 14 days to change your mind: V.PS from **€6.95/month**, renewal price included in what you see.
> - 👉 [See V.PS's live plan lineup and per-city prices](https://vps.hosting/?affid=1666)

## What "cheap yearly VPS" actually buys right now

The cheap end of the market has split into two price bands, and confusing them is how people end up disappointed.

The mainstream industry floor sits around $2/month — IONOS's entry plan is the frequent headline, and updated cheap-VPS roundups from late 2026 peg the bottom at $2.00/month with Vultr at $2.50 for 10 GB NVMe. At that level you're buying monthly-billed infrastructure from large providers, with uptime SLAs and refund policies but modest specs.

Below that sits the promo tier, and it's not close on price. DediRock ran a $7.00/year KVM special (2 GB RAM, 1 core, 30 GB SSD, 2 TB traffic) that pulled 68,000+ views and 2,200+ comments on LowEndTalk, sold out repeatedly, and came back. Its standing Promo VPS Saver is $8.88/year for 1 GB and 2 TB. RackNerd's New Year batch went as low as $11.29/year for 1 GB KVM, though its always-available 1 GB yearly plan is $21.99/year — the figure independent reviewers were still quoting as the floor in September 2026. ZgoCloud's LA Global Standard (2 GB/40 GB NVMe) runs $40/year, and BandwagonHost's classic 20G KVM is $49.99/year.

What you give up at $7–22/year is mostly guarantees. RackNerd's terms default to no refunds — payments are final outside case-by-case exceptions, verified against their ToS in October 2026 — and support is unmanaged, ticket-only. Community feedback on DediRock's promo boxes ranges from "solid little workhorse for basic tasks" to notes that they run slow under load. None of this makes them bad deals; it makes them final purchases.

## V.PS plans: six KVM families, priced by city

V.PS sells six KVM families — Cloud, Edge, Performance, Storage, Mini and Nano — across 11 datacenter locations: Hong Kong, Tokyo, Osaka, Singapore, Sydney, Frankfurt, Düsseldorf, Amsterdam, London, Tallinn and San Jose. Pricing varies by city and starts at €6.95/month. Every plan, regardless of family, includes:

- 1 dedicated IPv4 + 1 IPv6 address
- Full KVM virtualization on Proxmox VE — your own kernel, Docker that behaves
- 99.9% SLA
- 24x7 support, free at every tier (ticket-based; third-party reviews note there's no live chat)
- 14-day refund window on VPS products

Here's the lineup with the entry-tier specs that third-party plan trackers currently list. Configs and prices shift by city, so treat the checkout page as the final word:

| Plan | Entry config | Network & traffic | Monthly price (EUR) | Get it |
| --- | --- | --- | --- | --- |
| Cloud KVM — Starter | 2 vCPU / 1 GB / 20 GB SSD | 1 TB @ 1 Gbps | From €6.95 (San Jose from €8.95) | [See Cloud KVM city pricing](https://vps.hosting/?affid=1666) |
| Cloud KVM — Essential | 2 vCPU / 2 GB / 30 GB | 1 Gbps port | From €13.95 | [See Essential plans](https://vps.hosting/?affid=1666) |
| Edge KVM | 1 vCPU AMD EPYC / 2 GB / 20 GB NVMe | 1 TB, premium routed | From €8.95 | [See Edge plans](https://vps.hosting/?affid=1666) |
| Performance KVM | 2 vCPU EPYC / 2 GB / 30 GB NVMe | 1 TB @ 1.25 Gbps+, 2 backup slots | From €9.95 (Frankfurt) | [See Performance plans](https://vps.hosting/?affid=1666) |
| Mini / Nano | 1 vCPU / 1 GB | 500–600 GB @ 400–500 Mbps | Nano from €9.95/year | [See Mini plans](https://vps.hosting/?affid=1666) |
| Storage KVM | Storage-weighted configs | From 5 TB @ 1 Gbps | Priced per city at checkout | [See Storage plans](https://vps.hosting/?affid=1666) |

Two honesty notes on that table. Trackers disagree on a few entry-tier details — one review lists Cloud Starter as 1 core with 250 GB traffic, others say 2 cores and 1 TB — and the Cloud line scales through Pro and Premium tiers (up to 8 vCPU/8 GB per third-party listings) with configs that vary by location. Don't order off anyone's table, including this one; confirm at checkout.

Three things in the lineup deserve attention before you default to the cheapest row:

**The Edge plan is the quiet value pick.** For €2/month over Starter, Edge gets you AMD EPYC silicon and premium-routed network priority. One detailed V.PS review put it plainly: if you care about latency and stability at all, Edge is better value than Starter. A mail server, a small production site, or anything latency-sensitive justifies the difference immediately.

**Performance plans bundle backups.** The Performance family includes 2 automated backup slots and a guaranteed minimum port speed (1.25 Gbps and up, per the Frankfurt listings) — the only family where backups are part of the package. Cloud Starter and Edge don't include automatic backups, so if your data matters, either budget for snapshots elsewhere or step up a tier.

**The network underneath is real infrastructure.** V.PS runs on xTom's own backbone with direct peering at DE-CIX, AMS-IX and LocIX, plus Tier 1 upstreams, and BGP sessions are available if you want them. One caveat the marketing glosses over: "premium network" here means strong international and European routing — it is not a China-optimized CN2 GIA product, and the company makes no latency promises for mainland China. If China routing is your actual requirement, that's ZgoCloud or BandwagonHost territory, not this.

Also worth knowing how traffic is metered: incoming and outgoing both count against your allowance. A server that pulls 300 GB and pushes 300 GB has used 600 GB of a 1 TB plan. On the flip side, the bandwidth figures on V.PS's pricing page are guaranteed minimums, not "up to" values — a small but real distinction when you're comparing against promo hosts.

## The real math: $11/year promo vs €6.95/month

Run the annual numbers and the two tiers are roughly 10x apart. V.PS's entry price works out to **€83.40 over twelve months** — and because the listed price is the renewal price, that's the whole first-year story, no asterisk. RackNerd's standard 1 GB yearly plan is $21.99 with promo batches dipping to $11.29; DediRock's Saver is $8.88/year.

Why pay the difference? Four reasons that hold up against the verified specs:

1. **Refund protection.** V.PS gives you 14 calendar days on any VPS order, with the process documented up front. The promo tier is largely buy-and-pray.
2. **SLA and guaranteed port.** 99.9% uptime commitment and a guaranteed minimum port speed, versus advertised-but-unguaranteed specs at the bottom of the market.
3. **Location choice.** Eleven live cities versus whatever's in stock this promo cycle. RackNerd's Asia-optimized Los Angeles DC-02 sells out first in every batch, so if you need a specific location, the promo market may simply not have it when you're buying.
4. **Renewal stability.** €6.95 stays €6.95. Promo pricing at RackNerd is at least recurring rather than a first-year hook, but stock-limited plans can vanish, forcing a move to the higher standard list. Third-party reviews of V.PS also report periodic promotions — annual billing sometimes billed as 10 months' worth, seasonal sale pricing — though specific codes circulate in community posts and can't be treated as permanent.

If your workload is a VPN endpoint, a dev sandbox, or a low-traffic personal site, the promo tier does the job and the three-year savings are real money. If the box runs anything you'd hate to lose, the gap between tiers is effectively an insurance premium.

## The fine print that decides whether a "cheap" VPS is actually cheap

This is where most roundups stop, and it's where the expensive surprises live.

**The 14-day refund has more exceptions than the headline suggests.** The window is real, but the conditions matter: one refund per account ever; you must have used under 10 GB of traffic; renewals and flash-sale products are excluded; servers with active BGP/IX services, abuse reports or blacklisted IPs don't qualify. And critically, **crypto and bank transfer payments are non-refundable** — the refund right only works if you paid by card or PayPal. SSL certificates carry their own 30-day guarantee; domains are never refundable.

**Payment options are broad, which matters in this market.** PayPal, major cards and bank transfer are standard, and for a number of countries V.PS supports local methods: Alipay, iDEAL, Sofort, Giropay, Bancontact, EPS, Multibanco and Przelewy24. For readers in those regions, that removes the usual friction of budget VPS shopping, where card-only checkout is common.

**IP changes cost money after the first one.** One free replacement within 24 hours of activation, then €8 per change, once a month maximum, IPv4 only. If you're provisioning something that might get its IP blacklisted and swapped repeatedly, budget for it.

**Moving cities means migrating yourself.** There's no cross-location transfer: you deploy fresh in the new city, move your data, cancel the old server. With monthly billing that's an inconvenience; with a prepaid yearly promo plan elsewhere, it's money already spent.

**Every order passes fraud review.** Real legal name and billing address required, automated and manual checks, mismatches refused. Fine for almost everyone — just don't plan on a business alias.

**Promo stock is its own scarcity tax.** The cheapest RackNerd configurations sell out fastest in the most popular locations, repeatedly. The "$11.29/year" in a headline may have no buy button by the time you read it.

If any of these constraints touch your plans, read the terms before paying rather than after. 👉 [V.PS's order flow shows the per-city price and billing terms before you commit](https://vps.hosting/?affid=1666)

## FAQ

**Does V.PS sell yearly VPS plans?**
VPS billing is monthly in EUR, and the published pricing page doesn't show an annual prepay discount — the trade-off is that the listed price is also the renewal price, so a year simply costs 12x the monthly rate with no surprise. Community reviews report occasional promotions on longer billing cycles, and the Mini/Nano line is sold in annual terms from €9.95/year. The classic yearly-billing deals in this market come from RackNerd, DediRock, ZgoCloud and BandwagonHost, where annual prepayment is the business model.

**What's the cheapest legit yearly VPS that isn't a scam?**
Among offers verifiable as of late 2026: DediRock's Promo VPS Saver at $8.88/year and RackNerd's standard 1 GB plan at $21.99/year are the recurring benchmarks, with RackNerd promo batches hitting $11.29/year when in stock. "Legit" means reviewed and operating — not refundable. RackNerd's ToS makes payments final by default, so treat any of these as money spent.

**Can I get a refund on a cheap yearly VPS?**
Usually not. RackNerd refunds only case-by-case exceptions, and ZgoCloud's special-priced annual plans explicitly have no refund window. V.PS is the outlier here with a documented 14-day refund on VPS orders — subject to the exceptions above, including the 10 GB usage cap and the card/PayPal payment requirement.

**Is KVM important at this price?**
Insist on it even at the bottom of the market. KVM is full virtualization: your own kernel, working Docker, custom modules. Every provider named in this article — V.PS on Proxmox VE included — is KVM, which tells you where the floor has moved. If a deal looks too good and doesn't say KVM, that's usually why. One related gap to check: third-party reviews note that V.PS bundles DDoS protection with the Performance family rather than the entry tiers, so if your project attracts traffic it doesn't want, factor that into the tier choice.

## Which one should you actually buy

Sort yourself into one of three buckets and the decision is mechanical.

**The box is disposable** — VPN node, bot host, a sandbox you'll nuke and rebuild anyway. Buy the cheapest yearly promo in stock, in a location that isn't sold out, and mentally write off the $10–25. DediRock's $8.88/year Saver and RackNerd's 1 GB plan are the reference points.

**The box needs to stay up and you might need to leave** — a small client site, a game server friends actually use, anything with data you'd hate to re-create. Pay for the exit ramp: V.PS's 14-day refund, 99.9% SLA and month-to-month billing mean a bad decision costs one month, not one year. Start on Cloud Starter at €6.95; if latency turns out to matter, the €8.95 Edge plan is the cheapest upgrade that changes anything. 👉 [Pick your city and deploy a V.PS server here](https://vps.hosting/?affid=1666)

**You need China-optimized routes or specific premium lines** — none of the above is the answer as-is; that's CN2 GIA territory (ZgoCloud and BandwagonHost run those from roughly $45–52/year on specials), a different comparison for a different article.

One last practical note before you order anywhere: screenshot the price and terms on checkout day. Promo listings rotate, refund windows get consumed by usage caps faster than people expect, and the only version of "cheap" that matters is the one printed on your actual invoice.
