# DMIT CN2 GIA: What the Premium Route Actually Buys You, Full LAX Pro Pricing, and How to Pick a Tier Without Overpaying

Most people searching for DMIT CN2 GIA are standing in one of two places. Either they've been told that CN2 GIA is the only route worth paying for and want to know if that's true, or they already have a DMIT order page open, are staring at eight Premium tiers with quarterly minimums and a restock notice, and just want someone to tell them which one to take.

This covers both. The route facts first, because they explain the pricing, then the current Los Angeles lineup with real numbers, then the parts of the fine print that change the math — billing minimums, overage behaviour, and how DMIT differs from the cheaper CMIN2 and Tier 1 lines it also sells.

## What "CN2 GIA" actually means

CN2 is China Telecom's second-generation backbone, built as a separate network from the ordinary CHINANET path (AS4134) that most international traffic to China rides on. GIA stands for Global Internet Access, the premium tier of that network, announced under AS4809. The practical difference is capacity: GIA capacity is committed rather than best-effort, which is why it holds up during the 8–11pm window when ordinary Telecom transit turns into a mess of jitter and packet loss.

None of that is unique to DMIT. What matters is which parts of the path DMIT actually puts on AS4809, because "CN2 GIA" gets used loosely across the industry to describe anything with a GIA hop somewhere in it.

DMIT's Premium network on Los Angeles is documented as:

- China Telecom inbound: CN2 GIA (AS4809)
- China Unicom inbound: AS4837 direct
- China Mobile inbound: Hong Kong Mobile (AS58453)
- Return path for all three carriers: CN2 GIA (AS4809)

The return direction is the one that decides how a page feels in a browser. Having all three carriers come home over AS4809 is the part that distinguishes a genuinely China-optimized product from one that only optimizes Telecom.

If you want to check before paying, DMIT publishes a test IP for the Los Angeles Premium line: **154.17.30.96**. Bring your own traceroute and look for 59.43.x.x hops on the way back. That's the standard way to confirm GIA routing rather than taking a product page's word for it, and it costs nothing.

## Three locations, three platform generations

DMIT sells Premium (CN2 GIA) capacity in Los Angeles, Hong Kong, and Tokyo, on hardware it labels by CPU generation: AS3 (AMD EPYC 7003), AN4 (EPYC 9004), and AN5 (EPYC 9005).

The LAX AN4 line was retired in April 2026 when its hardware ran out, and AN5 is now the main Los Angeles lineup. That exit matters more than a normal product refresh, because AN4 carried the $9.99/month entry point people had been quoting for years. It's gone. The current entry tier is billed quarterly.

Hong Kong runs both AS3 and AN5 Premium hosts with identical network design; AN5 uses the newer EPYC platform, larger disks, and a higher price. Tokyo Premium exists on the same tiering structure, with the lowest entry price of the three locations — and the most erratic stock.

## The current LAX.AN5.Pro (CN2 GIA) lineup

All figures below come from DMIT's own order and cart pages. DMIT has re-tiered this line more than once in the past year, and some third-party tables floating around still show the previous generation's numbers, so treat the cart as the final word before you pay.

| Plan | vCPU | RAM | SSD | Traffic / port | After overage | Price | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| LAX.AN5.Pro.TINY | 1 | 2GB | 20GB | 1TB @ 1Gbps | 4Mbps unmetered | $37.99/quarter (~$12.66/mo), $119.99/yr | [order the TINY quarterly slot](https://www.dmit.io/aff.php?aff=12046&pid=100) |
| LAX.AN5.Pro.Pocket | 1 | 2GB | 40GB | 1.5TB @ 4Gbps | 4Mbps unmetered | $56.70/quarter (~$18.90/mo) | [order the Pocket quarterly slot](https://www.dmit.io/aff.php?aff=12046&pid=137) |
| LAX.AN5.Pro.STARTER | 2 | 2GB | 80GB | 3TB @ 10Gbps | 4Mbps unmetered | $38.90/mo | [check STARTER price and stock](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MINI | 4 | 4GB | 80GB | 5TB @ 10Gbps | 8Mbps unmetered | $79.90/mo | [check MINI price and stock](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MICRO | 4 | 4GB | 160GB | 7TB @ 10Gbps | 8Mbps unmetered | $110.90/mo | [check MICRO price and stock](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.MEDIUM | 6 | 8GB | 160GB | 14TB @ 10Gbps | 10Mbps unmetered | $289.90/mo | [check MEDIUM price and stock](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.LARGE | 8 | 16GB | 320GB | 25TB @ 10Gbps | 10Mbps unmetered | $499.90/mo | [check LARGE price and stock](https://www.dmit.io/aff.php?aff=12046) |
| LAX.AN5.Pro.GIANT | 12 | 24GB | 640GB | 50TB @ 10Gbps | 10Mbps unmetered | $1,009.90/mo | [check GIANT price and stock](https://www.dmit.io/aff.php?aff=12046) |

Every tier includes 1 IPv4 and 1 IPv6 /64 by default. The MEDIUM and above carry two or more IPv4 addresses. Traffic is counted in both directions, so a 1TB allowance on TINY is 1TB up plus down, not 1TB of downloads.

Two things to notice in that table. TINY and Pocket no longer offer monthly billing — quarterly is the minimum, which raises the cash you need to commit before you've tested anything. And the price curve is steep: the jump from STARTER to MEDIUM is a 7.5x increase in cost for roughly 4.5x the traffic and 4x the RAM.

If you'd rather see the whole Los Angeles Premium list with live stock than bounce between individual plan pages, DMIT exposes the filtered cart directly:

👉 [browse all Los Angeles Premium CN2 GIA plans with live availability](https://www.dmit.io/cart.php?aff=12046&region=los-angeles&generation=an5&network=premium)

Hong Kong Premium starts at **$39.90/month** for TINY (1 vCPU, 1GB RAM, 20GB SSD, 500GB @ 1Gbps) on both the AS3 and AN5 hosts, and climbs to $499.90/month for the GIANT tier. Tokyo Premium's entry plan has been listed around **$21.90/month** ($262/year), which makes it the cheapest way into any DMIT CN2 GIA route — when it's in stock, which is not most of the time. Treat those two figures as entry markers rather than a full quote and confirm the current tier list on the cart page.

## Why the prices moved, and what changed structurally

Comparing the old AN4 pricing to AN5 is not flattering. TINY went from $9.99/month to $37.99/quarter; STARTER from $29.90 to $38.90/month; GIANT from $619.99 to $839.90/month. Across the LAX Premium line, AN5 pricing sits roughly 20–30% above the tier it replaced, with LARGE moving furthest.

DMIT's own explanation for the broader drift is cost: IP rental prices rising to about 2.3x, plus power and data center costs. The company says it's shifting from renting IP space month-to-month toward outright purchase to stabilize long-term costs. Whether or not that satisfies you, the direction of travel is clear enough — this is a provider raising prices to protect a network it doesn't oversell, not one trying to win a race to $3/month.

What actually changed structurally:

- **Monthly billing disappeared from the two cheapest tiers.** TINY and Pocket now start at quarterly.
- **The old entry point is gone.** AN4's ~$88/year TINY was the reason a lot of people first tried DMIT. The AN5 equivalent is $119.99/year.
- **Bandwidth and traffic went up across the board.** Most mid and high tiers now ship 10Gbps ports.

## CN2 GIA vs CMIN2 vs Tier 1: don't pay for the wrong route

DMIT sells three network profiles out of the same buildings, and the single most common way to waste money here is buying Premium when Eyeball would have done the job.

| Network | Route profile | Best for | Price relationship |
| --- | --- | --- | --- |
| Premium (Pro) | Telecom AS4809, Unicom AS4837, Mobile via AS58453; GIA return on all three | Telecom-heavy audiences, latency-sensitive apps, anything where peak-hour stability is the product | Most expensive per GB |
| Eyeball (EB) | Three-network CMIN2 return (Telecom via AS9929/AS58807 balanced, Unicom AS9929, Mobile AS58807) | Mixed-carrier audiences, streaming, and mobile-first services where you want more traffic per dollar | Same sticker price as Pro on entry tiers, noticeably more traffic |
| Tier 1 (T1) | International BGP, no mainland China optimization | Audiences outside China. Also fine for development boxes and staging | Cheapest, biggest ports and traffic allowances |

The tell is in the entry-tier comparison. LAX.AN5.Pro.TINY and LAX.AN5.EB.TINY both start at $37.99/quarter, but the EB tier gives you 1.5TB at 2Gbps instead of 1TB at 1Gbps. If most of your users are on China Mobile, the EB line was built for exactly that and costs you the same.

Buy Pro when the audience is Telecom-heavy, when you're running something latency-sensitive like a game server or real-time relay, or when you've already tested and seen the Pro route outperform for your traffic. Buy Tier 1 when your users aren't in China at all — paying Premium rates to serve an American or European audience is a straight waste, and T1 gives you 5TB at 10Gbps for $14.90/month on the VOLUME line.

## Which tier to actually order

**LAX.AN5.Pro.TINY — $37.99/quarter, $119.99/year.** The cheapest 2GB RAM plan on any DMIT Premium route. One vCPU and 20GB of disk will run a personal blog, a lightweight API, a proxy endpoint, or a relay node. This is the plan to buy if you want to test CN2 GIA's value for yourself before committing real money. The quarterly minimum is the catch.

👉 [pick up the LAX.AN5.Pro.TINY plan and check its current restock status](https://www.dmit.io/aff.php?aff=12046&pid=100)

**LAX.AN5.Pro.Pocket — $56.70/quarter.** Doubles the disk to 40GB and lifts the port to 4Gbps and traffic to 1.5TB, for about $6 more per month than TINY. If you keep running out of the TINY allowance, skip STARTER and look here first — you get more traffic than STARTER's 3TB? No, you don't; you get less traffic but at a lower effective monthly cost. STARTER's advantage is the 3TB allowance and the 10Gbps port at $38.90/month, which is a better long-term deal if you're month-to-month.

**LAX.AN5.Pro.STARTER — $38.90/month.** The most balanced entry into monthly billing on the Pro line: 2 vCPU, 80GB, 3TB, 10Gbps. Worth it if you don't want to tie up a quarter's payment up front.

**MINI and above.** At $79.90/month for MINI you're paying for capacity, not just route quality, and the per-GB economics improve as you climb. These tiers make sense when you're running production workloads with steady throughput. They do not make sense for a site getting a few thousand visits a day — you're buying bandwidth headroom you'll never touch.

One honest note about the high end: DMIT's stock on LAX Premium turns over, and MINI has been the tier most often sitting at out-of-stock. If you're planning around a specific tier, check availability before you build a migration schedule on it.

## Buying: payment, coupons, and the restock rhythm

DMIT accepts Alipay, PayPal, and Visa/MasterCard credit cards, and its support tickets work in Chinese. That Alipay support is a real practical difference for buyers who don't want to fight an overseas card through a bank's fraud team on a Sunday night.

Coupons do exist, and they're structured in a way that trips people up. DMIT issues recurring discount codes tied to a specific line *and* billing cycle — a code that takes 10% off LAX Pro monthly orders won't do anything on a Hong Kong Tier 1 quarterly order. At checkout you enter the code in the promo field and hit **Validate Code**; if the code doesn't apply to your cart, it simply won't validate. Codes circulating on forums and coupon roundups frequently expire, and this year's LAX restocks have mostly been sold at listed price without a public code, so budget for full price and treat any working code as a bonus rather than the plan.

On stock: LAX Premium plans sell out and get restocked in waves, and the entry tiers go first. There's no reliable public restock calendar, so the workable approach is to check the cart page on the day you actually need the machine, not the day you start researching.

## The limits worth reading before you pay

**Overage means throttling, not shutdown.** Burn through your monthly allowance and DMIT drops you to a fixed rate — 4Mbps on TINY through STARTER, 8Mbps on MINI and MICRO, 10Mbps on the upper tiers — and keeps the server online with unmetered transfer at that speed. For a personal site or relay, a 4Mbps trickle beats a suspended VPS. For a busy production box, it's a hard ceiling you should plan around.

**Traffic is bidirectional.** Both directions count against the allowance. If you're pricing out a high-traffic workload, halve the effective allowance before you do the math.

**IP replacement.** Community documentation of DMIT's policy describes one free IP change every 15 days, with additional changes at $5 each after that, and a self-service change feature in the client area. Confirm the current terms in your control panel rather than relying on a reseller's summary — policies like this get revised.

**SLA and support.** DMIT advertises a 99% uptime figure rather than the 99.9% some competitors print. That's a lower number stated honestly, but it's still a commitment you should weigh against the workloads you're putting on it.

## FAQ

**Is DMIT's CN2 GIA real CN2 GIA, or a marketing label?**
Test it yourself. Trace the return path from a mainland connection and look for 59.43.x.x hops; DMIT's published routing for the Premium line specifies AS4809 GIA on the return leg for all three carriers. A traceroute costs you five minutes and settles the question for your specific ISP and city.

**CN2 GIA or CMIN2 if I mostly serve mobile users?**
CMIN2, at least to start. The Eyeball tiers cost the same at entry level and give you more traffic, and the return path is mobile-native. Pro's advantage concentrates on Telecom and on peak-hour consistency. If your traffic split is genuinely mixed, buy one of each and measure.

**Can I pay monthly on the cheap plans?**
No. LAX.AN5.Pro.TINY and Pocket are quarterly minimum. STARTER and everything above still offer monthly billing.

**What hardware am I getting?**
AMD EPYC 9005 (AN5) on the current Los Angeles line, with DDR5 memory and NVMe-class SSD storage. The older AS3 host (EPYC 7003) is still sold in Hong Kong alongside AN5.

**Do I need to worry about losing my IP to blocking?**
Any provider with native mainland-facing routes eventually deals with this. DMIT's IP-change policy exists for that reason. If a blocked IP takes your service down entirely, that's an argument for keeping a second small instance on a different line rather than for expecting a provider to solve it.

## The short version

CN2 GIA is a route quality, not a performance guarantee, and DMIT's Premium line is one of the more defensible implementations of it because all three carriers return over AS4809 rather than just Telecom. The bill for that is around 20–30% above the previous hardware generation, a quarterly minimum on the cheapest tiers, and stock that goes in and out. For a Telecom-heavy audience, a latency-sensitive service, or anyone who's already lost evenings to peak-hour congestion, the arithmetic works. For an audience outside China, it doesn't — take the Tier 1 line, and put the difference into more traffic.
