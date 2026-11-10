# American Mandala, Episode 1: producing a short with Claude and DaVinci Resolve

A case study of making a 90-second Instagram episode where I supplied the creative and Claude did the
hands-on editing inside DaVinci Resolve Studio, through an MCP server.

**Status:** Episode 1 is finished and delivered to the series owner for posting. It is the first of a planned 10-episode series.

## The result

- **Format:** 1.5-minute vertical episode for Instagram.
- **What I made:** the script and copy, and the imagery.
- **What Claude did in Resolve:** cutting, titling, color, audio mixing, mastering, and export, directed by me.
- **Effort:** about 4 days of focused work, roughly 3 hours a day, spread over 10 calendar days.
- **Delivered to:** the series owner, who posts it.

## How it worked

```
My copy and images ─► Claude (via the DaVinci Resolve MCP server) ─► Resolve timeline ─► finished master
                                  ▲                                         │
                                  └──── I review each version and direct the next change ────┘
```

I used the open-source [DaVinci Resolve MCP server](https://github.com/samuelgursky/davinci-resolve-mcp)
by Samuel Gursky (MIT license), which exposes Resolve's scripting API to an AI assistant. I did not write
that server. My work was the creative content and the direction of the edit: I described what I wanted,
Claude made the changes in Resolve, and I reviewed the result and gave the next instruction.

## Evidence from the edit log

The tool records every timeline change it makes. From that log for this project:

- **368 logged edits** across **69 timeline versions** between Oct 31 and Nov 10, 2026.
- Edit mix: **85 color/LUT changes**, **77 compositing changes**, **51 clip deletions**, **36 fade changes**,
  **30 markers**, **23 tracks added**, **17 transforms**, and **6 title insertions** (including Fusion titles).
- **Iteration is visible in the version names.** The cut went through named versions such as
  "Reel 1 - rebuilt to transcript", "FINAL v2 (longer bumper)", "FINAL v4 (tight open)",
  "FINAL v5 (new ending)", "FINAL v6 (corner caption)", and "FINAL v8 (no typed card)". Each was a creative
  decision I made and Claude carried out.

The log covers timeline edits only. Audio mixing, mastering, and export are not in it: those were done on
Resolve's Fairlight page, also directed through the same MCP server.

## What I learned

- **Direction beats instruction count.** The good versions came from clear creative decisions ("tight
  open", "no typed card"), not from step-by-step button clicking.
- **Version everything.** Duplicating the timeline before each change made it safe to try bold edits and
  roll back.
- **Review is the job.** The AI can execute fast, so my value was knowing what the episode should feel like
  and catching what was off.
- **Be specific.** Vague instructions get vague edits. The more exact the direction, the fewer rounds it takes.
- **Time and tokens go fast.** Long sessions burn usage quickly, so I compress context and keep each
  request focused instead of letting the conversation grow.

## What's next

- **Episodes 2 to 10.** The series is planned as 10 episodes, and I will produce each one the same way,
  reusing what worked on Episode 1.

*No footage is included here. The series belongs to its owner, who is fine with it being described publicly.*
