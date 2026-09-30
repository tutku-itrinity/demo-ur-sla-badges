# Acme Payments API

<picture><source media="(prefers-color-scheme: dark)" srcset="https://badge.uptimerobot.com/sla/28c610335dc8b380d76b45afbc63b7d0.svg?theme=dark"><img src="https://badge.uptimerobot.com/sla/28c610335dc8b380d76b45afbc63b7d0.svg?theme=light" alt="Uptime SLA"></picture>

A fast, reliable REST API for processing payments, refunds, and payouts.


## Reliability & SLA

We take uptime seriously. Our production API is monitored every 60 seconds by
[UptimeRobot](https://uptimerobot.com), and the badges above update automatically
with our real uptime over the last 24 hours, 7 days, 30 days, and 90 days.

| Service              | SLA target | Current (30d)                                   |
|----------------------|------------|-------------------------------------------------|
| Payments API         | 99.95%     | ![30d](<SLA_BADGE_URL_API_30D>)                 |
| Webhooks delivery    | 99.9%      | ![30d](<SLA_BADGE_URL_WEBHOOKS_30D>)            |
| Merchant dashboard   | 99.9%      | ![30d](<SLA_BADGE_URL_DASHBOARD_30D>)           |

For live status, incident history, and maintenance windows, see our
[status page](<STATUS_PAGE_URL>).

## Quick start

```bash
curl https://api.acmepay.example/v1/charges \
  -H "Authorization: Bearer $ACME_API_KEY" \
  -d amount=2500 \
  -d currency=usd
```

## Installation

```bash
npm install @acmepay/node
```

```js
import Acme from "@acmepay/node";

const acme = new Acme(process.env.ACME_API_KEY);
const charge = await acme.charges.create({ amount: 2500, currency: "usd" });
```

## Add an SLA badge to your own project

Want badges like these? Here's how we set ours up:

1. Create a monitor for your service in UptimeRobot.
2. Open the monitor and go to the **SLA badge** section.
3. Pick the time period (24h, 7d, 30d, 90d) and copy the Markdown or HTML snippet.
4. Paste it at the top of your README.

Markdown:

```markdown
[![Uptime](<SLA_BADGE_URL>)](<STATUS_PAGE_URL>)
```

HTML (useful if you want to control size or alignment):

```html
<a href="<STATUS_PAGE_URL>">
  <img src="<SLA_BADGE_URL>" alt="Uptime" height="20">
</a>
```

## Support

- Status page: <STATUS_PAGE_URL>
- Docs: https://docs.acmepay.example
- Email: support@acmepay.example

## License

MIT
