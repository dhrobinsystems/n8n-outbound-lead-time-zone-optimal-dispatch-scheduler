# ⚠️ Disclaimer & Liability Limitation

**Use at your own risk.** The code, workflows, and scripts in this repository (`n8n-outbound-lead-time-zone-optimal-dispatch-scheduler`) are provided for educational and architectural demonstration purposes.

## No Liability

The author and dhRobin Systems accept no responsibility or liability for any direct, indirect, incidental, or consequential damages that result from using, misusing, or deploying these scripts. This includes, without limitation, messages or calls dispatched at the wrong local time, on weekends or holidays, or to recipients in a different timezone than resolved; duplicate, missed or delayed dispatches; contact with people who have not consented or have opted out; telemarketing, anti-spam or privacy regulatory claims and penalties; deliverability or sender reputation damage; exposure of contact data, tokens or endpoint URLs; incorrect queue or CRM updates; service interruptions; and API rate-limit or quota exhaustion.

## No Warranty

All software, n8n JSON blueprints, JavaScript modules and prompts are provided "AS IS", without warranty of any kind, express or implied. This includes, but is not limited to, warranties of merchantability, fitness for a particular purpose, and non-infringement.

No warranty is given that timezones resolved from explicit fields, phone numbers, country or region fields, or email domains are correct for any recipient; that the area-code, country-code, region or ccTLD tables are complete or current; that the Node.js time-zone database on your n8n host reflects current daylight-saving rules; that weekend, regional-weekend or holiday handling matches any market; that the schedule runs on time; or that the dispatch endpoint, queue endpoint or notifications behave as expected.

## Production Testing Required

Always test thoroughly in an isolated staging environment, such as a test sequence, a test dialer campaign and a queue you control, with `SANDBOX_MODE=true`, `DRY_RUN=true` and `DISPATCH_ENABLED=false` enabled, before you connect live CRM, queue, sequencer, dialer or Slack credentials. Test several fixed evaluation times, including Friday evenings, holidays and daylight-saving weekends, review every `low` and `fallback` resolution, and confirm that only leads inside their local window reach the dispatcher.

Treat every resolved timezone as an estimate. Store an explicit timezone for recipients wherever you can, and hold rather than guess for phone channels.

## Third-Party APIs & Compliance

You alone are responsible for complying with the terms of service, rate limits, data privacy regulations (GDPR/CCPA and equivalents), electronic marketing and telemarketing laws (TCPA, the Telemarketing Sales Rule, state calling-hour and quiet-day rules, CAN-SPAM, PECR, CASL, the Australian Spam Act and equivalents), and security policies of your CRM, queue, sequencer, dialer, Slack and any connected services. That includes:

- confirming consent or another lawful basis for each channel and recipient before dispatch;
- honouring do-not-contact flags, suppression lists and national or state do-not-call registries, which this workflow does not check;
- keeping the configured business window inside every legal calling and messaging window that applies to each recipient's location;
- giving recipients accurate sender identification and a working opt-out;
- securing, rotating and restricting access to every token and endpoint URL;
- limiting access to n8n execution data, which contains contact points, and applying a retention period that matches your policies;
- reviewing every automatically dispatched lead and every queue or CRM update.

## No Affiliation

Slack, n8n and Node.js are trademarks of their respective owners. This project is independent and is not affiliated with, endorsed by, or sponsored by any of them. All leads, names, email addresses, phone numbers and identifiers in the fixtures, sample payloads and pinned data are fictitious; phone numbers use ranges reserved for fictional use.

## Not Professional Advice

Nothing in this repository constitutes legal, telemarketing-compliance, privacy, security, or financial advice. Consult qualified professionals for your specific circumstances.

---

Released under the MIT License. Copyright (c) 2026 DH Robin (dhRobin Systems). See [LICENSE](LICENSE).

Full text: DISCLAIMER.md · Licensed under the MIT License. License: MIT © 2026 dhRobin Systems · Provided as-is, see the disclaimer.
