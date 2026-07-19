# Web Scraping API with Proxies: How to Pick the Right One? Which Plan Is Actually Worth It? How to Avoid Getting Blocked Mid-Project? (Includes a Full ScraperAPI Plan Breakdown and Live Discount Codes)

If you've ever tried to scrape a real website at any real scale, you already know the wall I'm about to describe. The first 50 requests work fine. Then request 51 hits a Cloudflare challenge page. Then 200 returns a 403. Then your IP gets banned and your script that ran for two hours is suddenly dead in the water. You Google "web scraping api with proxies," and a dozen products show up — all promising the world, none of them priced the same way, and most of them quietly hiding the real cost behind words like "credits" and "multipliers."

This article is for the person who's tired of guessing. I'm going to walk through what a **web scraping API with proxies** actually is, what to look for, why most people get the pricing math wrong, and then dig into one specific option in detail — ScraperAPI — including every plan on their pricing page, the real per-request cost once multipliers kick in, what users say about it, and the discount codes that actually work right now.

## What a Web Scraping API with Proxies Actually Does (and Why It's Not the Same as Buying Proxies)

There's a common confusion worth clearing up first. A "web scraping API with proxies" is not the same thing as buying a proxy list. When you buy raw proxies — datacenter, residential, mobile — you get IP addresses. You still have to write the scraper, manage rotation, handle headers, deal with CAPTCHAs, retry failed requests, and babysit the whole thing when a target site updates its anti-bot defenses.

A scraping API bundles all of that behind a single HTTP call. You send a URL, the service routes your request through a rotating proxy pool, manages headers and fingerprints, solves or bypasses CAPTCHAs, optionally renders JavaScript, and hands you back the HTML or structured JSON. You pay per request (or per "credit," more on that later) instead of per GB of bandwidth.

The trade-off is control versus convenience. Raw proxies give you maximum control and the lowest possible cost per page if you know what you're doing. A scraping API costs more per request but removes roughly 90% of the infrastructure pain. For most small-to-mid teams, the API route wins because the time saved babysitting proxies is worth more than the price difference.

## How to Actually Evaluate a Web Scraping API with Proxies

Before naming any product, here's the rubric I use. Most comparison articles skip this and jump straight to "here are ten tools," which is why people end up on the wrong plan.

- **Proxy pool size and type.** Residential IPs (from real ISPs) bypass anti-bot systems better than datacenter IPs. Mobile IPs bypass them best of all. Look for at least a few million residential IPs in the pool.
- **Rotation and session control.** Pure rotation gives you a new IP per request. Sticky sessions let you hold the same IP for a sequence of requests (essential for logged-in flows). Both should be available.
- **Geotargeting.** Can you pick a country? A city? Some sites only return correct data when the request comes from a specific region.
- **JavaScript rendering.** Most modern sites are JS-heavy. If the API can't render JS, you'll get empty divs instead of content.
- **CAPTCHA and anti-bot handling.** Cloudflare, DataDome, PerimeterX, Turnstile — the API should handle these without you writing bypass logic.
- **Pricing transparency.** This is where most providers hide the real cost. Look for: per-request or per-credit pricing, multipliers for premium features, and whether overage is allowed or you're forced to upgrade.
- **Concurrency limits.** How many simultaneous requests can you make? This often matters more than total credits for time-sensitive jobs.
- **Success rate, not just volume.** A million credits that fail 40% of the time is worse than 500K credits that succeed 97% of the time.
- **Uptime guarantee and support.** Look for at least 99.9% uptime and responsive support. Scraping is production infrastructure for a lot of teams.

Keep that list handy. Every claim a scraping API makes should map back to one of those bullets.

## ScraperAPI: The Web Scraping API with Proxies That Hides the Hard Parts

ScraperAPI is one of the older and more popular options in this space. Founded in 2018 by Daniel Ni (a Yale grad and ex-Wall Street developer who also writes the TLDR tech newsletter), it bootstrapped to roughly $3M in revenue and 10,000 customers before being acquired by SaaS.group in August 2020. As of April 2026 it acquired Traject Data — the company behind Rainforest API and SerpWow — which folded a stack of structured SERP and e-commerce APIs into the same credit economy.

The pitch is simple. One HTTP endpoint, send a URL, get HTML or JSON back. ScraperAPI handles proxy rotation, CAPTCHA solving, JavaScript rendering, header management, and retries. Their proxy pool is advertised at over 20 million rotating IPs across more than 30 countries, with at least 5 million residential IPs maintained at all times. They claim a 97% average success rate on standard requests, a 99.9% uptime guarantee, and only charge for successful requests — failed requests don't burn credits.

A basic call looks like this:

bash
curl "http://api.scraperapi.com/?api_key=APIKEY&url=http://httpbin.org/ip"


Add `render=true` for JavaScript rendering, `country_code=us` for geotargeting, `premium=true` to force residential IPs, `session_number=123` for sticky sessions, or `ultra_premium=true` for the hardest targets. The standard pool already includes residential proxies as fallback, so for many sites you don't need to pay for premium.

## The Full ScraperAPI Plan Comparison Table

This is the part most articles get wrong. They copy the headline credit numbers and move on. The table below includes **every plan currently listed on ScraperAPI's pricing page** — Hobby, Startup, Business, Scaling, Professional, Advanced, and the sales-led Enterprise tier — with the actual concurrent thread caps, geotargeting scope, and overage handling. Annual billing takes 10% off every plan.

| Plan | API Credits / Month | Concurrent Threads | Geotargeting | Key Perks | Price (Monthly) | Annual (10% off) | Get Started |
|------|---------------------|--------------------|--------------|-----------|-----------------|--------------------|-------------|
| **Free Trial** | 5,000 (7 days) | 5 | Standard | No card required | $0 | — |  [Start Free Trial](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | 100,000 | 20 | US & EU | 30-day analytics | $49/mo | ~$44/mo |  [Get Hobby Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Startup** | 1,000,000 | 50 | US & EU | Standard analytics | $149/mo | ~$134/mo |  [Get Startup Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Business** | 3,000,000 | 100 | Global (country-level) | Unlimited analytics | $299/mo | ~$269/mo |  [Get Business Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Scaling** (Most Popular) | 5,000,000 | 200 | Global | Pay-As-You-Go overage | $475/mo | ~$428/mo |  [Get Scaling Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Professional** | 10,500,000 | 300 | Global | Priority support + PAYG | $975/mo | ~$878/mo |  [Get Professional Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Advanced** | 21,500,000 | 500 | Global | Priority routing + PAYG | $1,975/mo | ~$1,778/mo |  [Get Advanced Plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| **Enterprise** | 22,000,000+ | 500+ | Global + custom | Dedicated support + Slack + PAYG | Custom | Custom |  [Contact Sales](https://www.scraperapi.com/contact-sales/?fp_ref=coupons) |

A few things worth pointing out before you scroll past this table:

- **There is no permanent free tier.** You get 5,000 free credits for 7 days, then a 1,000-credit/month forever-free plan with 5 concurrent connections. That's enough to test the API, not enough to run anything real.
- **Pay-As-You-Go overage only unlocks on Scaling and above.** If you're on Hobby, Startup, or Business and you exhaust your credits mid-month, you're forced to upgrade. There's no overflow billing. This is a deliberate design choice — it's also the most common reason people complain about ScraperAPI on Reddit.
- **Concurrency is a separate lever from credits.** A Hobby user with 100K credits and 20 threads can't match the throughput of a Scaling user with 5M credits and 200 threads, even if neither ever hits their credit ceiling. If your job is latency-sensitive (say, scraping SERPs that change hourly), the thread cap matters as much as the credit count.
- **Annual billing is a flat 10% off every plan**, no strings. If you're confident you'll use the service for a year, that's the cheapest legitimate discount available.

👉 [You can compare plans side by side and grab the annual discount here.](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## The Credit Multiplier: Why "100,000 Credits" Doesn't Mean "100,000 Scrapes"

This is the single most misunderstood thing about ScraperAPI, and frankly about most credit-based scraping APIs. The headline credit count is **not** the number of pages you can scrape. Each request type spends a different number of credits based on how hard it is to fulfill.

Here's the official multiplier table, pulled directly from ScraperAPI's documentation:

| Request Type | Credits per Request |
|--------------|---------------------|
| Standard request (no parameters) | 1 |
| `premium=true` (force residential) | 10 |
| `render=true` (JS rendering) | 10 |
| `screenshot=true` | 10 |
| `premium=true` + `render=true` | 25 |
| `ultra_premium=true` (hardest targets) | 30 |
| `ultra_premium=true` + `render=true` | 75 |
| Cloudflare / Turnstile / DataDome / PerimeterX bypass | 10 |

And on top of that, certain high-value domains carry **fixed multipliers** regardless of which parameters you set:

| Domain | Credits per Request |
|--------|---------------------|
| Amazon (e-commerce) | 5 |
| Google / Bing SERP (all subdomains) | 25 |
| LinkedIn | 30 |

Parameters like `country_code`, `device_type`, `wait_for_selector`, `session_number`, `output_format`, `keep_headers`, and `autoparse` cost **zero** extra credits.

Now do the math. A Hobby user paying $49/month for 100,000 credits, scraping JavaScript-rendered pages, gets:

$$\frac{100{,}000 \text{ credits}}{10 \text{ credits per render}} = 10{,}000 \text{ rendered pages}$$

That's the real capacity — 10,000 pages, not 100,000. Effective cost per rendered page is around $0.0049.

A Business user paying $299/month for 3,000,000 credits, scraping Google SERPs at 25 credits each, gets:

$$\frac{3{,}000{,}000 \text{ credits}}{25 \text{ credits per SERP}} = 120{,}000 \text{ SERP requests}$$

Effective cost per SERP request: about $0.0025.

This is why the pricing page can keep the same headline numbers ($49 / $149 / $299) for years — when anti-bot defenses get harder, the multiplier absorbs the cost, not the sticker price. It's a clever model. It's also a model that quietly burns through your credits if you don't read the multiplier table before you start.

ScraperAPI gives you two ways to check costs before you commit: an in-dashboard **Domain Multiplier lookup** tool, and a programmatic endpoint:


https://api.scraperapi.com/account/urlcost?api_key=...&url=...&render=true


Every API response also includes a `sa-credit-cost` header showing the exact credit cost of that request. Use these. Most "ScraperAPI ate my credits in a day" complaints come from people who never checked.

## Features That Matter for Real-World Scraping

Beyond the pricing math, here's what ScraperAPI actually delivers under the hood:

- **20M+ rotating proxies across 30+ countries**, including at least 5 million residential IPs. The standard pool already mixes datacenter and residential, so you only pay for `premium=true` when you really need it.
- **12 standard geotargeting countries**: US (5.1M IPs), Canada, UK, Germany, France, Spain, Brazil, Mexico, India (3.5M IPs), Japan, China, and Australia. Other countries are available on higher-tier plans.
- **JavaScript rendering** via headless browser, triggered with a single `render=true` parameter.
- **CAPTCHA handling and anti-bot bypass** built in. Cloudflare, Turnstile, DataDome, and PerimeterX are handled automatically on standard requests.
- **Sticky sessions** via `session_number=123`. Sessions expire 15 minutes after last use.
- **Unlimited bandwidth.** You're billed on requests, not bytes.
- **99.9% uptime guarantee** on every plan, including Hobby.
- **Only successful requests cost credits.** Failed requests refund automatically.
- **24/7 support**, with priority routing on Professional and above.
- **Analytics dashboard** showing request volume and credit usage — 30 days on lower tiers, unlimited on Business and above.

## Use Cases Where ScraperAPI Actually Wins

Based on the feature set and the multiplier math, ScraperAPI fits cleanly into a few buckets:

1. **E-commerce price monitoring.** Amazon is only 5 credits per request, and structured data endpoints make product extraction straightforward. A Business plan can pull hundreds of thousands of Amazon pages per month.
2. **SERP data collection.** Google and Bing cost 25 credits each, which sounds steep until you do the per-SERP math — about $0.0025 on Business, cheaper than most dedicated SERP APIs.
3. **SEO and rank tracking.** Combined with the geotargeting, you can pull rankings from specific countries without maintaining your own proxy fleet per region.
4. **Market research at moderate scale.** Anything up to a few million requests per month falls comfortably in the Business-to-Scaling range.
5. **Real estate and travel listing aggregation.** These are typically JS-heavy and benefit from `render=true`. Just budget for the 10x credit multiplier.
6. **AI agent data feeds.** ScraperAPI added a dedicated "AI & Automation" solution page in 2026, positioning itself as a backend for LLM agents that need live web data.

Where ScraperAPI is **not** the right fit:

- **Hardcore Cloudflare-protected targets requiring mobile IPs.** ScraperAPI doesn't offer mobile proxies. If you're scraping sites that block datacenter and residential IPs, you'll need a mobile-proxy specialist.
- **Sub-$50/month budgets.** The cheapest real plan is $49. Crawlbase and Zyte both start cheaper.
- **People who hate credit multipliers.** If you want flat per-request pricing with no surprises, look at Zyte's pay-for-success model or a pay-per-request marketplace.

## What Real Users Say

ScraperAPI publishes testimonials on their rotating proxies page from a handful of named users. Cristina Saavedra, Optimization Director at SquareTrade, credits the support team for patience debugging her first scraper. Ilya Sukhar — founder of Parse and a Y Combinator partner — calls it "a dead simple API plus a generous free tier" and "a good example of how developer experience can make a difference in a crowded category." Alexander Zharkov, a fullstack JavaScript developer, highlights low cost and tech support that responds within 24 hours.

Third-party review aggregators tell a similar story with the usual caveats. Most positive reviews center on developer experience and documentation quality. The recurring complaints, also predictable, are about the credit multiplier catching people off guard and the lack of a permanent free tier beyond the 1,000-credit/month allowance.

The honest summary: people who read the docs and model their costs before signing up tend to love it. People who sign up based on the headline credit count and then enable `render=true` on everything tend to feel burned.

## How to Get Started Without Burning Money

If you're new to ScraperAPI, here's the cheapest possible learning path:

1. **Sign up for the free trial.** You get 5,000 credits and 7 days, no card required. That's enough to test against your actual target sites.
2. **Use the URL cost endpoint** before you scrape anything at scale. `https://api.scraperapi.com/account/urlcost?api_key=...&url=...&render=true` returns the exact credit cost.
3. **Try the standard pool first.** Most sites don't need `premium=true`. Save the 10x multiplier for sites that actually require residential IPs.
4. **Use `render=true` only when necessary.** If the data you need is in the initial HTML, don't pay 10 credits for a rendered page.
5. **Pick annual billing if you're confident.** The flat 10% off is the easiest legitimate discount.

👉 [Start with 5,000 free credits and test against your real targets first.](https://www.scraperapi.com/?fp_ref=coupons)

## Active Discount Codes and Promotional Offers

A quick note on discount codes, because there's a lot of noise here. Multiple coupon aggregators (Saver.com, Knoji, ValueCom, ColorMango, Freelance-Stack) list ScraperAPI promo codes, with claimed discounts ranging from 10% to 28% off. The most consistently reported working code is a 10%-off-first-month offer. Beyond that:

- **Annual billing** is the only guaranteed discount — flat 10% off every plan, no code needed.
- **The affiliate landing page itself** is configured for coupon access (`fp_ref=coupons`), which suggests ScraperAPI runs periodic promo codes through affiliate channels. Check the signup flow for any active offer banner.
- **Enterprise deals** are negotiated directly with sales and typically include volume-based discounts, dedicated support, and custom credit pools.

I'm not going to print specific promo code strings here because most aggregator-listed codes either expire fast or only apply to specific plans. The reliable discount is annual billing, and the affiliate-linked page is the right place to check for any active promo.

## How ScraperAPI Compares to the Alternatives

A quick comparison against the other major players in the "web scraping API with proxies" space, based on publicly listed pricing:

- **ScraperAPI** — best for general-purpose scraping at moderate scale, strong documentation, transparent credit system once you understand the multiplier.
- **ScrapingBee** — similar credit model with stealth features; slightly cheaper at the Business tier but the same 1–75 credit multiplier problem.
- **Zyte** — cheapest raw HTTP requests at $0.00013 each, but browser rendering is 7–8x more expensive. Best if you're already in the Scrapy ecosystem.
- **Bright Data** — most complete platform (72M+ IPs, Scraping Browser, datasets) but the $499/mo Growth plan is a high barrier and pricing gets complex.
- **Oxylabs** — strong for e-commerce and SERP, 100M+ residential IPs, but most plans require a sales call.
- **Apify** — best for no-code scraping via 3,000+ pre-built Actors; credit consumption varies wildly by Actor.
- **Crawlbase** — cheapest entry at $29/mo, good for side projects, smaller proxy pool.

The pattern: if you want simplicity and you're OK with the credit model, ScraperAPI is the cleanest default. If you want the absolute cheapest HTTP requests and you're technical, Zyte. If you want enterprise-grade infrastructure and you have the budget, Bright Data or Oxylabs. If you want no-code, Apify.

## The Verdict on ScraperAPI as a Web Scraping API with Proxies

ScraperAPI is not the cheapest option and not the most feature-complete option. What it is, consistently, is the most *legible* option. The pricing page is public, the multiplier table is documented, the trial is real, and the API is genuinely a single endpoint you can call from `curl`. For a developer or data team that wants to scrape at moderate scale without maintaining proxy infrastructure, it removes exactly the right amount of complexity.

The credit multiplier is the catch. It's not a hidden fee — it's documented in plain sight — but it does mean you have to model your real cost before you commit. If you're scraping plain HTML, 100K credits really is 100K pages. If you're scraping JS-rendered pages, it's 10K pages. If you're scraping LinkedIn, it's about 1,333 pages. The same plan, three very different real capacities.

If your use case is e-commerce monitoring, SERP collection, market research, real estate listings, or any moderate-scale scraping where you want someone else to handle proxies and CAPTCHAs, ScraperAPI is a safe, well-documented default. Start with the free trial, model your costs with the URL cost endpoint, and only commit to a paid plan once you know your real per-page cost.

👉 [Test it free with 5,000 credits, no card required.](https://www.scraperapi.com/?fp_ref=coupons)

## Final Checklist Before You Buy Any Web Scraping API with Proxies

If you scrolled to the end, here's the short version of everything above:

- Pick a provider whose pricing model you can actually model. Credits-with-multipliers are fine if the multiplier table is public.
- Run your real target URLs through a free trial before paying anything. Never trust marketing-page success rates on their own.
- Check whether the plan forces upgrades when you exhaust credits, or allows Pay-As-You-Go overage. Forced upgrades are the most common surprise bill.
- Verify the proxy types available. Residential is the baseline; mobile is the gold standard for hard targets.
- Confirm geotargeting scope on your tier. Lower tiers often restrict you to US/EU.
- Read the concurrency cap, not just the credit count. Time-sensitive jobs care about throughput, not volume.
- Use annual billing if you're confident in the product. It's almost always the largest guaranteed discount.

ScraperAPI clears all those boxes for moderate-scale, general-purpose scraping. It won't be the right answer for everyone — no scraping API is — but it's the right answer more often than the comparison articles make it sound.

👉 [Compare all ScraperAPI plans and grab the 10% annual discount here.](https://www.scraperapi.com/pricing/?fp_ref=coupons)
