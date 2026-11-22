# AGENTS.md — jonathanmccallum-ko (Korean mirror of jonathanmccallum.com)

Korean mirror site. Same theme and design as the main site (Paper Light),
content translated into Korean, meaning-first. Repo: streamjonathan/jonathanmccallum-ko.
Live (when approved): ko.jonathanmccallum.com. Proof: jonathanmccallum-ko.pages.dev.

## Mission

Mirror jonathanmccallum.com in Korean — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Korean site goes live on ko.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Register: warm, plain 해요체 throughout. First person 저는. Second person
  usually omitted; 여러분 where the reader is addressed directly. No 합쇼체
  (-습니다), no 반말. Jesus 예수님, God 하나님, Christ 그리스도. "Jonathan"
  stays in Latin script, as in the Japanese proof.
- Names (never vary): 아슬란, 나니아, 루시, 디고리, 티리안, 아담과 하와, 케어 패러벨,
  하얀 마녀. Book titles use the published Korean editions (시공주니어):
  『나니아 나라 이야기』, 『마법사의 조카』, 『마지막 전투』, 『천국과 지옥의 이혼』
  (홍성사, 김선형 역). 『우주 3부작』 is a descriptive rendering for The Space
  Trilogy — no published edition title verified; Jonathan to confirm.
- Bible verses: none of the 5 articles contains a direct Bible quotation, so no
  verse text was reproduced. The bread/water of life lines are Jonathan's
  paraphrase (echoing John 6:35 / 4:14) — 생명의 떡 / 생명의 물 — never presented
  as quoted Scripture. KRV (개역한글, public domain) wording is recorded in
  work/korean-proof/glossary-ko.md if he wants exact quotations later.
- No direct Lewis quotations appear either; none were invented.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
