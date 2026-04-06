# HR.skill

<div align="center">

> *"Thank you for your interest in this position. After careful consideration, we have decided to move forward with other candidates whose qualifications more closely align with our current needs. We will keep your resume on file for future opportunities."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

You sent out a hundred applications.<br>
Ninety-nine came back as rejections. One was left on read.<br>
Every rejection was perfectly worded, warmly phrased, and completely uninformative.<br>
You asked why you were rejected. HR said "after careful consideration."<br>
You asked for feedback. HR said "we'll keep your resume on file."<br>
You never heard from them again.<br>

**Now it's your turn.**

<br>

Summon HR.skill. Generate a perfectly crafted, emotionally devastating rejection letter.<br>
Or enter HR persona mode — answer every question without saying anything at all.

[Features](#features) · [Install](#install) · [Examples](#examples) · [Rejection Museum](#rejection-museum) · [Custom Persona](#custom-persona) · [中文](README.md)

</div>

---

## Features

### Rejection Letter Generator
Provide a job title and candidate name. Receive a letter that:
- Warmly compliments the candidate while rejecting them
- Explains nothing
- Promises to "keep their resume on file"
- Ends with "all the best" or "we wish you the best in your search"

### HR Persona Mode
Have a conversation with HR. HR will:
- Answer every question without providing any actual information
- Describe every red flag as a "growth opportunity"
- Say "competitive compensation" when you ask about salary
- Say "great work-life balance" when you ask about overtime
- Say "we're a fast-paced environment" when they mean "we're understaffed"
- Say "culture fit" when they mean anything they can't legally say

### Style Options

| Style | Keywords | Signature phrase |
|-------|----------|-----------------|
| Big Tech (CN) | 感谢投递 | "After comprehensive evaluation of your background..." |
| Startup (CN) | 双向奔赴 | "We regret that we couldn't embark on this journey together..." |
| Corporate (EN) | move forward | "We've decided to move forward with other candidates..." |
| Startup (EN) | culture fit | "We don't see a mutual fit at this time..." |
| Recruiter | resources | "I've forwarded your resume and will be in touch!" *(never heard from again)* |

---

## Install

```bash
git clone https://github.com/Schlaflied/hr-skill
cp hr-skill/SKILL.md ~/.claude/commands/hr.md
```

Then in Claude Code:
```
/hr
```

---

## Examples

### Generate a rejection letter

```
/hr Reject a candidate who applied for a UX Designer role. English, corporate style. Make it sound like we really agonized over this decision.
```

Output:
> Dear [Candidate],
>
> Thank you so much for taking the time to interview with us for the UX Designer position. It was a genuine pleasure learning more about your background and experience.
>
> After careful deliberation, we have made the difficult decision to move forward with another candidate whose experience more closely aligns with our current needs. This was truly not an easy decision — the team was impressed by your work.
>
> We will absolutely keep your resume on file and hope to stay in touch. We wish you all the best in your search and have no doubt you'll find a wonderful opportunity soon.
>
> Warm regards

### HR Persona Mode

```
/hr Enter HR mode. I'm going to ask you some questions.
```

```
Me: Why did the last person in this role leave?
HR: We really value each team member's individual growth journey, and we fully support people as they explore new directions. We're now excited to find someone who can grow with us long-term!
```

```
Me: What's the salary range?
HR: We offer a competitive compensation package that's tailored to each candidate's unique background and experience. We'd love to discuss the specifics once we're both aligned on mutual interest!
```

```
Me: Is this role remote-friendly?
HR: We're a hybrid team that really values in-person collaboration, especially for the creative energy it brings. We're flexible and work with each individual to find a rhythm that works!
*(Actual answer: 5 days in office)*
```

---

## Custom Persona

Don't want a generic HR? Describe the specific HR you've suffered from:

```
/hr Custom persona: Her name is Jessica. She works at a Series B startup. She says "we move fast" and "we're a team of doers." She ends every email with "excited for what's ahead!" and has never given a single piece of constructive feedback in her life.
```

Or create a config file in `colleagues/`:

```markdown
---
name: Jessica
company: Series B startup
language: en
style: startup-enthusiastic
---

Speech style: relentlessly positive, zero substance.
Loves: "move fast", "team of doers", "exciting roadmap", "ownership mentality"
Hates: direct questions, salary discussions, explaining why someone was rejected
Sign-off: always "excited for what's ahead! 🚀"
```

---

## Rejection Museum

Collected from the real world. A tribute.

**The Classic (Corporate EN)**
> "Thank you for your interest in [Company]. After careful consideration, we have decided to pursue other candidates whose qualifications more closely align with our current needs. We will keep your application on file for future opportunities."

**The Empathetic One (Startup EN)**
> "We really enjoyed getting to know you and were genuinely impressed by your background. Ultimately, we're looking for someone who's a stronger culture fit for where we are as a team right now. We'd love to stay in touch!"

**The One That Hurts (CN)**
> "感谢您参与本次招聘流程。经过综合评估，我们认为您与岗位的匹配度暂未达到预期，此次暂不考虑。期待未来有机会合作。"

**The Recruiter's Last Words**
> "Great talking to you! I've shared your profile with the team and will follow up as soon as I have an update!"  
> *(Last seen: online 847 days ago)*

**The One That Took 6 Months**
> "We apologize for the delay in getting back to you. After an extended review process, we've decided to move in a different direction. We truly appreciate your patience."

---

## Acknowledgements

Inspired by [titanwings/colleague-skill](https://github.com/titanwings/colleague-skill).  
Raw material sourced from the collective suffering of job seekers worldwide.

---

<div align="center">

MIT License · Built by someone with too many rejection emails and too much free time

</div>
