# LoreGap — downloads

Signed and notarised builds of **LoreGap**, a local-first macOS study trainer for the
**Claude Certified Developer – Foundations** certification.

This repository holds releases only; it contains no source code.

![LoreGap after a wrong answer: what you chose, the correct answer, the explanation, and
the confidence question underneath](screenshot.png)

The question at the bottom is what sets it apart. You say how sure you were *before*
answering, after seeing whether you were right. Everything else — mastery, review timing,
what counts as a misconception — is built on that one signal.

## What it does

LoreGap is not a quiz app. It answers a narrower question: *what do you believe you know
that you actually do not?*

After every answer you say how sure you were beforehand. That single signal is what the
rest is built on:

- **Wrong plus confident** is treated as a misconception, not an ordinary mistake, and
  comes back sooner and more often. Believing something false is worse than knowing you
  do not know.
- **Right plus guessing** does not buy you a long silence. A lucky answer is not mastery.
- Mastery is tracked **per concept**, not per question, so answering the same question
  again proves nothing.
- Review brings back what is due, and tells you why each concept is on the list.
- Progress is weighted by the exam's published blueprint: being weak in a domain worth a
  third of the exam is not the same as being weak in one worth three percent.

Everything is local. No account, no network, no telemetry. Your answers stay on your Mac.

## Download

**[Latest release](https://github.com/neosergio/loregap-releases/releases/latest)**

Requires macOS 14 or later. A universal binary: Apple Silicon and Intel.

Every build is signed with a Developer ID certificate and notarised by Apple, so it opens
without a Gatekeeper warning. The notarisation ticket is stapled to the app itself, not
only to the disk image, so the first launch works with no network connection.

## Verifying a download

```sh
shasum -a 256 LoreGap-0.2.dmg     # compare against the checksum in the release notes
spctl --assess --type execute --verbose=2 /Applications/LoreGap.app
```

A correct result reads `accepted` and `source=Notarized Developer ID`.

## What to tell me about

This is an early build and the question bank is still small: **twenty-three questions**,
covering 97.4% of the exam's published weight but only a few questions in each domain. You
will run out of new material quickly. That is expected and it is not the thing to report.

What is worth reporting is the loop:

- Does rating your confidence feel natural, or like a chore in the way?
- When Review brings a concept back, does the timing feel right — too soon, too late?
- Does Progress tell you what to study next, or only how you did?
- Did it surface something you were wrong about and did not realise?
- Anything that felt slow, confusing, or that you expected and did not find.

Impressions are as useful as bugs. "I did not understand what this screen wanted" is a
finding.

## Feedback

[Issues](https://github.com/neosergio/loregap-releases/issues) is the place. No template,
no form — a sentence is fine.
