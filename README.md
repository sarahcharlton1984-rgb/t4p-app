# The Director's Position

The Tax 4 Pros diagnostic app, served at **https://app.tax4pros.co.uk**.

Static, no build step, no framework. GitHub Pages serves `index.html` from `main`.

## Do not edit index.html here

It is generated. The app is authored in the `youtube-autopilot` repo and built by
`build_position_page.py`, which adds the page head, the email gate and the GHL
lead capture. Editing this copy means the next build silently overwrites it.

To change the app: edit the source, run the builder, copy `index.html` across,
push.

## Every figure has a source

All rates and thresholds come from `content/TAX_FIGURES_LIVE.md` in the
`youtube-autopilot` repo, each one verified with a dated source and an
independent cross-check before it went on screen.

**Every rate in this app changes at a Budget.** The next one is 28 October 2026.
A tax tool showing last year's figures is worse than no tool, so the app is
re-verified and rebuilt the day after the Chancellor sits down.

## Lead capture

Name and email unlock the stage detail. The capture posts to the same GHL
inbound webhook as the pay calculator (Calculator Lead Capture workflow), along
with the figures that qualify the lead: total tax, effective rate, CGT on a
sale, IHT exposure, companies controlled, sale and departure intent, VAT status
and IR35 regime.
