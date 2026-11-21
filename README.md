# Cheap UK VPS: How Low Do Prices Really Go, Why Does the Second Year Cost More, and Which Spec Tier Do You Actually Need? (Full Price Benchmark Table)

A cheap UK VPS currently sits between £2 and £4 a month at the entry level. IONOS advertises from £2/month, and OVHcloud's VPS-1 in its UK datacentre is £3.31 ex. VAT (£3.97 incl. VAT) for 2 vCores, 4 GB RAM and 40 GB NVMe. That is the real floor for a machine with a UK IP address and full root access.

What those headline numbers hide is the part that decides your actual bill: how long the low price lasts, whether VAT is in or out, and what "unlimited traffic" means once you read the terms. Below is a benchmark table pulled from four providers' own UK pages, then the checks that separate a genuinely cheap VPS from one that gets expensive in month four.

> **Quick pick:** Most personal projects (a blog, a small API, a VPN endpoint, a staging box) run fine on 2 vCPU / 4 GB. Move to 4–6 vCPU / 8–12 GB when you're running Docker with several containers, a CI runner, or more than a handful of sites. Game servers and busy shops start at 8 vCPU / 24 GB.
> 👉 [See AkkoCloud's current UK VPS plans and prices](https://bit.ly/akkocloud)

## UK VPS price benchmark: what each tier actually buys

All figures below are the prices shown on each provider's own UK page at the time of writing. Currency and tax treatment differ between brands, so read the "price and basis" column before comparing anything.

| Plan | vCPU | RAM | Storage | Price and basis | Notes |
| --- | --- | --- | --- | --- | --- |
| OVHcloud VPS-1 | 2 | 4 GB | 40 GB NVMe | £3.31 ex. VAT / £3.97 incl. VAT | 500 Mbps, daily backup included |
| OVHcloud VPS-2 | 4 | 8 GB | 75 GB NVMe | £6.29 ex. VAT / £7.55 incl. VAT | 1 Gbps |
| OVHcloud VPS-3 | 6 | 12 GB | 100 GB NVMe | £9.01 ex. VAT / £10.81 incl. VAT | 2 Gbps |
| OVHcloud VPS-4 | 8 | 24 GB | 200 GB NVMe | £17.34 ex. VAT / £20.81 incl. VAT | 3 Gbps |
| Contabo Cloud VPS 4 | 4 | 8 GB | 100 GB SSD | €4.40/mo (list €5.50), 24-month price | 200 Mbit/s, 1 snapshot |
| Contabo Cloud VPS 6 | 6 | 12 GB | 200 GB SSD or 100 GB NVMe | €6.00/mo (list €7.50), 24-month price | 300 Mbit/s, 2 snapshots |
| Contabo Cloud VPS 8 | 8 | 24 GB | 300 GB SSD or 150 GB NVMe | €11.20/mo (list €14.00), 24-month price | 600 Mbit/s, 3 snapshots |
| Contabo Cloud VPS 12 | 12 | 48 GB | 400 GB SSD or 200 GB NVMe | €20.00/mo (list €25.00), 24-month price | 800 Mbit/s, 3 snapshots |
| Contabo Cloud VPS 18 | 18 | 96 GB | 600 GB SSD or 300 GB NVMe | €39.20/mo (list €49.00), 24-month price | 1 Gbit/s, 3 snapshots |
| IONOS VPS | Varies by tier | Varies by tier | Varies by tier | From £2/mo | Up to 1 Gbit/s, 1 IPv4 + 1 IPv6/80 included |
| Fasthosts Windows VPS 2 | 2 | 4 GB | 120 GB NVMe | £14/mo for 3 months (list £22) | 1 Gbit/s, 1 IPv4 included |
| Fasthosts Windows VPS 4 | 4 | 8 GB | 240 GB NVMe | £27/mo for 3 months (list £42) | 1 Gbit/s, 1 IPv4 included |

Two structural facts jump out of that table. OVHcloud is the only one showing both tax figures side by side, and Contabo is the only one quoting a discount tied to a fixed contract length rather than a calendar window. Everything else you have to work out yourself.

## The low price has an expiry date, and it is written on the page

Contabo shows €5.50 struck through next to €4.40 on Cloud VPS 4, with "for the first 24 months" underneath. Same pattern on the bigger plans: €14.00 becomes €11.20, €25.00 becomes €20.00, €49.00 becomes €39.20. The discount is real, and it is paid for with a two-year commitment. Over those 24 months you save €26.40 on VPS 4 compared with the list price. After month 24, you are a customer on whatever the list price is at that point.

Fasthosts runs the same trick on a shorter clock. Windows VPS 2 lists at £22/month and shows £14/month "for 3 months". Do the arithmetic on year one: three months at £14 (£42) plus nine months at £22 (£198) comes to £240. If the £14 had held for all twelve months, it would have been £168. The £72 gap is the cost of not reading the expiry line.

So when you land on a plan page, look for the words that usually sit in small grey type under the price: *for the first N months*, *renewal price*, *regular price*, *list price*, *after the introductory period*. If none of those appear, that usually means the displayed price is the ongoing one. It is worth a support ticket to confirm before you commit a year.

## Normalise three things before you compare any two prices

**Tax.** OVHcloud lists VPS-1 as £3.31 ex. VAT or £3.97 incl. VAT. That is a 20% spread on the same product. IONOS prices the additional IPv4 at £5 excl. VAT and Cloud Backup at £0.045 per GB per month excl. VAT. Contabo quotes euros with a contract discount baked in. Pick one basis, most usefully the amount that actually leaves your bank account each month with VAT included, and convert everything to it.

**Billing cycle.** Contabo's €4.40 is a 24-month price; the same server on a shorter term costs more. A monthly-billed plan at a slightly higher headline rate can beat a two-year lock-in if there's any chance you move or outgrow the box within a year. Cheapest per month and cheapest per project are different questions.

**Traffic terms.** "Unlimited" is a marketing word with a policy behind it. Contabo's unlimited in and out transfer is explicitly subject to its Fair Usage Policy. OVHcloud's unlimited traffic carries a regional quota: in the Asia-Pacific locations (Mumbai, Singapore, Sydney), VPS-1 gets 500 GB a month, VPS-2 and VPS-3 get 1 TB, VPS-4 gets 3 TB, and past that the port drops to 10 Mbps. UK-datacentre plans don't carry that quota, but the rule matters the moment you add a second node in Asia.

👉 [Check AkkoCloud's London node and its billing options](https://bit.ly/akkocloud)

## Which spec tier fits which job

**A blog, a static site, or one small WordPress install.** 2 vCPU / 4 GB / 40 GB is enough, and the £2–£4 bracket exists precisely for this. OVHcloud VPS-1 gives you NVMe and a daily backup at that size. Don't buy more cores to run PHP and MySQL for one site; you'll be paying for idle capacity.

**Several sites, a few Docker containers, or a CI runner.** This is the 4–6 vCPU / 8–12 GB band. Contabo Cloud VPS 6 at €6.00 and OVHcloud VPS-3 at £9.01 ex. VAT land in the same neighbourhood with different trade-offs: Contabo gives more RAM per pound and a slower port, OVHcloud gives NVMe across the range and 2 Gbps.

**A Minecraft or CS:GO server.** Start at 8 vCPU / 24 GB, then look at port speed rather than core count alone. OVHcloud VPS-4 runs a 3 Gbps public port; Contabo Cloud VPS 18 runs 1 Gbit/s with double the RAM and cores. Game server load is spiky and latency-sensitive, so the network side matters as much as the spec sheet.

**A busy shop.** 8 vCPU / 24 GB is the floor, and the deciding factor is usually the backup arrangement rather than raw CPU. See the next section.

👉 [View AkkoCloud's full plan list and configuration tiers](https://bit.ly/akkocloud)

## Windows changes the maths

Pick Windows only when you need the GUI or a Microsoft stack (.NET, SQL Server, RDP-based administration). The licence cost is inside the monthly price, so a Windows VPS at £14/month is not comparable to a Linux VPS at £4/month.

There are also hard floors. IONOS states that Plesk needs a minimum of 20 GB storage on Linux and 32 GB on Windows, which rules out the smallest tiers if you want a control panel. OVHcloud's Local Zone VPS runs Linux only: Windows, Plesk, cPanel and Docker are all unsupported there, along with preinstalled apps, additional storage, monitoring, additional IPs, load balancers and managed databases. If any of those are on your list, that product line is off the table regardless of price.

Fasthosts sells Windows across its VPS range with Windows Server 2016 through 2025 available, one IPv4 included and unlimited IPv6, on either 1-month or 12-month contracts. The £14 entry price applies to the first three months, as covered above.

## Backups, snapshots and the upgrade rule nobody reads

Backup is where cheap plans quietly diverge.

OVHcloud includes a daily backup of the previous 24 hours, held on a rolling 7-day basis and replicated three times within the same datacentre. Premium backup and snapshots are paid extras. Contabo gives you snapshots instead of a managed backup schedule: one on Cloud VPS 4, two on VPS 6, three on VPS 8 and above. IONOS sells Cloud Backup from Acronis separately at £0.045 per GB per month excl. VAT, so a server with 100 GB of data adds £4.50 a month.

Upgrades also have rules. OVHcloud lets you raise the configuration from the control panel in one click, but only within the same datacentre, and downgrading means ordering a new VPS and migrating your data yourself. That matters at purchase time: sizing up later is easy, sizing down is a project.

## Where AkkoCloud fits, and what to verify before paying

AkkoCloud (akkocloud.com) lists a London node among its locations, alongside Frankfurt and San Jose, running KVM virtualisation with CN2 GIA routing toward Asia. That routing is the reason to consider it if your audience is split between the UK and mainland China: a generic London VPS serves UK visitors well and adds noticeable latency for users in Shanghai, while a CN2 GIA path is built for the reverse case.

Its plan table is quoted in CNY and covers monthly, quarterly and annual billing, so don't put its headline number next to a GBP price without converting and deciding how you'll treat VAT. Four things are worth confirming on the page before you enter payment details:

1. **Is the plan you selected actually in London?** Datacentre location is normally a dropdown at checkout, and the default is not always the UK.
2. **What does the price become at renewal?** Annual plans frequently revert to a higher rate in year two.
3. **How many IPv4 addresses are included?** One is standard almost everywhere; extra addresses are a paid add-on at most providers.
4. **What is the refund window, and does it cover the billing term you chose?** A 7-day window is meaningless on a 12-month prepayment if you only discover a problem in week three.

👉 [Compare AkkoCloud's UK options at current prices](https://bit.ly/akkocloud)

## Decision rules

- **One small site, lowest possible bill:** 2 vCPU / 4 GB, monthly billing, £2–£4 range.
- **Several containers or a handful of sites:** 4–6 vCPU / 8–12 GB. Contabo Cloud VPS 6 at €6.00 and OVHcloud VPS-3 at £9.01 ex. VAT both sit here.
- **Game server or busy shop:** 8 vCPU / 24 GB and up, and check port speed as well as cores.
- **Windows required:** budget £14–£27/month at Fasthosts after the three-month window, and check the 32 GB storage minimum if you want Plesk.
- **UK plus Asian visitors:** a UK node with premium routing back to Asia is worth paying a little more for; a plain London box is not.

Three things to confirm on the checkout page before you pay: whether the price includes VAT, what it becomes at renewal, and whether backup is included or billed separately. Those three answers change the true monthly cost far more than the headline number does.

👉 [Check AkkoCloud's current UK VPS pricing](https://bit.ly/akkocloud)
