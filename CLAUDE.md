# Jamiya

A ROSCA (jam'iya) app built on transparency instead of company credit risk. Every member
sees the same ledger and the full payout schedule from day one.

## Product decisions (interview, 2026-09-20)

- Market: UAE / GCC first, AED.
- Circles: private (invite friends and family) first. Platform-matched public circles
  ("Jamiya Match") later.
- Payout order: fixed when the circle launches. Shuffle or organizer-assigned. Never
  changes afterwards.
- Credit risk: members carry it, Jamiya never guarantees payouts. Safeguards instead:
  one contribution held as deposit per member (returned after the last cycle), trust
  score per member, low-score members placed in the second half of the order, deposit
  funds the payout if a member stops paying and they lose their slot.
- Revenue: small fee per cycle (prototype shows 1% per contribution).
- Look: English, modern Gulf fintech. Arabic later.
- Reference competitor: Money Fellows (Egypt), which guarantees payouts and carries
  credit risk. Jamiya deliberately does not.

## Prototype

- `jamiya-prototype.html`: single-file clickable prototype, phone-width, sample data.
  Screens: home dashboard, circles list, circle detail (cycle progress, payout schedule,
  payment ledger grid, safeguards), create circle (live summary, invite code), pay flow
  (fee breakdown, method, success receipt that updates the ledger).
- Published artifact: https://claude.ai/artifact/M7ExTjiN5qcNMsFjgNx7uv
- Design tokens: green accent (#0E6B54), gold reserved for the user's own payout,
  semantic paid/due/late colors separate from the accent. Sora headings, IBM Plex Sans body.

## Open questions

- Payment rails for the UAE (card vs Aani bank transfer vs direct debit).
- Licensing: holding deposits and routing pooled funds may need a regulated partner.
- Trust score inputs beyond on-time payments.
- Fee model detail: charged on contribution, on payout, or both.

## Handoff

2026-09-20: interview done, prototype v1 published. Awaiting Sultan's feedback on the
four screens. No git repo yet, no backend, no real payments.
