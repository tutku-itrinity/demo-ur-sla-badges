# Acme Payments API

<picture><source media="(prefers-color-scheme: dark)" srcset="https://badge.uptimerobot.com/sla/28c610335dc8b380d76b45afbc63b7d0.svg?theme=dark"><img src="https://badge.uptimerobot.com/sla/28c610335dc8b380d76b45afbc63b7d0.svg?theme=light" alt="Acme Payments API uptime SLA"></picture>

A fast, reliable REST API for processing payments, refunds, and payouts.

## Reliability & SLA

We take uptime seriously. Our production API is monitored around the clock by
[UptimeRobot](https://uptimerobot.com), and the badge above updates automatically
with our real uptime. It also follows your GitHub theme, switching between light
and dark mode.

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

Want a badge like ours? Here's how to set it up:

1. Create a monitor for your service in [UptimeRobot](https://uptimerobot.com).
2. Open the monitor and go to the **SLA badge** section.
3. Copy the embed snippet.
4. Paste it at the top of your README.

The snippet looks like this. It shows the dark badge in dark mode and the light
badge otherwise:

```html
<picture><source media="(prefers-color-scheme: dark)" srcset="https://badge.uptimerobot.com/sla/<YOUR_BADGE_ID>.svg?theme=dark"><img src="https://badge.uptimerobot.com/sla/<YOUR_BADGE_ID>.svg?theme=light" alt="Uptime SLA"></picture>
```

Prefer plain Markdown? Use a single theme:

```markdown
![Uptime SLA](https://badge.uptimerobot.com/sla/<YOUR_BADGE_ID>.svg?theme=light)
```

## Support

- Docs: https://docs.acmepay.example
- Email: support@acmepay.example

## License

MIT
