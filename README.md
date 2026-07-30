# answerweave-holding

Temporary holding page for the **answerweave.ai** apex, served by GitHub Pages.

It exists to replace GoDaddy's parking page — an ad-supported page we don't control,
on our canonical brand domain, that search engines can index as "AnswerWeave".

## Deliberately indexable

Every other host on the domain — `app.`, `sandbox.`, `qa.` — sends
`X-Robots-Tag: noindex, nofollow` at the edge. This page is the single exception, on
purpose: one clean branded page starts establishing the domain for the brand name before
launch, and gets *replaced* by the real homepage rather than competing with it.

## DNS

`CNAME` in this repo pins the custom domain. The apex needs four A records at the
registrar (GitHub Pages publishes these):

    185.199.108.153   185.199.109.153   185.199.110.153   185.199.111.153

## Retiring it

Delete this repo and the A records when the real marketing site ships. Nothing else
depends on it.

Source of record: `deploy/holding-page/` in the ai-website-assistant repo (Azure DevOps).
