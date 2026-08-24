**Chapter 3.4 Build a Library of Skills for Real Work**

- [Contract Issue Spotter for a Lawyer](#contract-issue-spotter-for-a-lawyer)
- [Campaign Brief Builder for a Marketer](#campaign-brief-builder-for-a-marketer)
- [Interview Question Pack for HR](#interview-question-pack-for-hr)
- [Listing Draft from Verified Facts for a Real Estate Agent](#listing-draft-from-verified-facts-for-a-real-estate-agent)
- [Account Meeting Brief for a Salesperson](#account-meeting-brief-for-a-salesperson)
- [Lesson Adaptation for a Teacher or Trainer](#lesson-adaptation-for-a-teacher-or-trainer)
- [Manuscript Consistency Check for a Publisher or Author](#manuscript-consistency-check-for-a-publisher-or-author)
- [Weekly Decision and Action Review for Operations](#weekly-decision-and-action-review-for-operations)


# Contract Issue Spotter for a Lawyer

A lawyer or legal operations team might review many contracts using the same internal checklist. A useful skill can perform the first structured pass.

Property|Value
---|---
**Skill name**|Contract Issue Spotter
**Purpose**|Review a draft agreement against an approved checklist and prepare an issue list for a lawyer.
**Inputs**|•	Draft contract.<br/>•	Approved review checklist.<br/>•	Optional client or matter context.
**Procedure**|1.	Read the contract without rewriting it.<br/>2.	Check each item in the approved checklist.<br/>3.	Quote or identify the relevant clause.<br/>4.	Mark each checklist item as Present, Missing, Unclear, or Needs Legal Review.<br/>5.	Explain why an item was flagged using neutral language.<br/>6.	End with questions for the reviewing lawyer.
**Output**|A table of issues followed by a short question list.
**Acceptance criteria**|•	Every checklist item is covered.<br/>•	Every finding points to contract text or clearly states that no matching text was found.<br/>•	The skill does not invent a clause.<br/>•	The skill does not tell the client what legal decision to make.<br/>

*Table 3.4A: Contract Issue Spotter skill specification for a lawyer.*

> **Sample files**: A completed Contract Issue Spotter skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/contract-issue-spotter/.

A prompt could be as simple as:
```
Review the attached supplier agreement using my Contract Issue Spotter skill.
Use the standard supplier-contract checklist attached to this project.
Do not rewrite the agreement. Produce the issue table and questions for legal review.
```

This is a strong skill because the repeatable part of the work is the checklist pass. The lawyer still decides whether an issue matters, what advice to give, and what language to negotiate.

> **Watch out**: Legal work can involve confidential and privileged information. Use only the Claude plan, workspace, retention settings, and connected systems approved for the matter. A skill does not change your professional or confidentiality obligations.

# Campaign Brief Builder for a Marketer

Marketing teams often receive a mixture of product notes, research, audience information, and deadlines, then turn them into a standard campaign brief. That transformation is ideal for a skill.

Property|Value
---|---
**Skill name**|Campaign Brief Builder
**Purpose**|Turn approved source material into a consistent campaign brief without adding unsupported claims.
**Inputs**|•	Product or service facts.<br/>•	Target audience.<br/>•	Campaign goal.<br/>•	Channels.<br/>•	Deadline.<br/>•	Brand or claims rules.
**Procedure**|1.	Extract only facts supported by the source material.<br/>2.	State the campaign goal in one sentence.<br/>3.	Summarize the target audience without inventing demographics.<br/>4.	Propose three message themes grounded in the approved facts.<br/>5.	List evidence or source material behind each theme.<br/>6.	Flag missing information that blocks a safe claim.<br/>7.	Produce the brief in the team's standard format.
**Output**|A one- or two-page campaign brief.

*Table 3.4B: Campaign Brief Builder skill specification for a marketer.*

> **Sample files**: A completed Campaign Brief Builder skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/campaign-brief-builder/.

A marketer could then use a second skill, such as Channel Adaptation, to turn an approved message into versions for LinkedIn, email, a landing page, and an internal sales note.

This shows an important design idea: do not make one giant "Marketing" skill. Make a chain of smaller skills:
```
Research summary -> Campaign brief -> Channel adaptation -> Final brand check
```

Each skill has a job that is easy to understand and test.

> **Real-world example**: A software company launches a new reporting feature. The Campaign Brief Builder uses the product manager's approved notes and customer research. It proposes message themes, but it flags "saves hours every week" because the source material does not contain evidence for that claim. The marketer can then decide whether to remove the claim or obtain supporting data.

# Interview Question Pack for HR

Hiring contains repeated administrative work, but it also contains decisions that affect people. A skill should help structure the process without deciding who deserves a job.

Property|Value
---|---
**Skill name**|Interview Question Pack
**Purpose**|Create a consistent interview question set from an approved job description and competency framework.
**Inputs**|•	Final job description.<br/>•	Approved competency framework.<br/>•	Interview length.<br/>•	Required questions used for every candidate.
**Procedure**|1.	Extract the role's stated responsibilities and competencies.<br/>2.	Use the required questions exactly as written.<br/>3.	Add a small number of role-specific questions tied to the job description.<br/>4.	Add neutral follow-up prompts for incomplete answers.<br/>5.	Produce a scoring guide based only on job-related evidence.<br/>6.	Remove questions about protected or irrelevant personal characteristics.<br/>7.	End with a reminder that the interviewer owns the assessment
**Output**|A structured interview pack.

*Table 3.4C: Interview Question Pack skill specification for HR.*

> **Sample files**: A completed Interview Question Pack skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/interview-question-pack/.

A companion Candidate Evidence Summary skill could summarize what a candidate stated in a resume or application against the same job-related criteria. It should identify evidence and gaps, not rank applicants automatically.
```
Use the Interview Question Pack skill with the attached approved job description.
The interview is 45 minutes.
Keep the six organization-wide questions unchanged.
Add no more than four role-specific questions.
```

> **Good practice**: Keep the same core criteria for all candidates applying for the same role. A skill is useful here because consistency can improve both efficiency and fairness.

# Listing Draft from Verified Facts for a Real Estate Agent

A real estate agent repeatedly turns property information into listings, brochures, and online descriptions. The risky part is not the writing. It is accidentally inventing or exaggerating a property feature.

Property|Value
---|---
**Skill name**|Verified Property Listing
**Purpose**|Draft property marketing text from verified facts while keeping unknown information clearly marked.
**Inputs**|•	Property fact sheet.<br/>•	Approved measurements and features.<br/>•	Target listing channel.<br/>•	Length limit.<br/>•	Agency style guide.
**Procedure**|1.	Extract facts from the supplied property information.<br/>2.	Separate verified facts from opinions or missing information.<br/>3.	Draft a clear description within the channel's length limit.<br/>4.	Avoid claims that cannot be checked from the supplied information.<br/>5.	Do not infer school quality, neighborhood safety, future property values, or demographic characteristics.<br/>6.	End with a list titled Facts to Verify Before Publishing if anything is missing or uncertain.
**Output**|Listing text plus a verification list.

*Table 3.4D: Listing Draft from Verified Facts skill specification for a Real Estate Agent.*

> **Sample files**: A completed Listing Draft from Verified Facts skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/listing-draft-from-verified-facts/.

This skill can be paired with a Viewing Follow-up Draft skill that takes the agent's own notes and creates a polite follow-up message without inventing what the buyer said.

> **Real-world example**: The source sheet says "rear garden" but does not give its direction. The skill should not describe it as a "sunny south-facing garden." It should simply say "rear garden" and flag the direction as unknown if that detail matters.

# Account Meeting Brief for a Salesperson

Salespeople often spend time gathering the same categories of information before an account call.

Property|Value
---|---
**Skill name**|Account Meeting Brief
**Purpose**|Turn approved account information and public research into a one-page pre-meeting brief.
**Inputs**|•	Account notes.<br/>•	Previous meeting notes.<br/>•	Public company information.<br/>•	Purpose of the upcoming meeting.
**Procedure**|1.	Separate confirmed internal facts from public information.<br/>2.	Summarize the recent relationship history.<br/>3.	List open actions from previous meetings.<br/>4.	Identify two or three relevant public developments.<br/>5.	Prepare questions rather than assumptions about the customer's needs.<br/>6.	Flag stale or conflicting information.<br/>7.	End with the three things the salesperson should know before the call.
**Output**|A one-page briefing document.

*Table 3.4E: Account Meeting Brief skill specification for a Salesperson.*

> **Sample files**: A completed Account Meeting Brief skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/account-meeting-brief/.

This skill becomes much more useful when *Chapter 3.5*'s MCP connectors can reach an approved CRM, shared drive, or other source. The skill defines how to prepare the brief. A connector supplies where the information comes from. Keep those ideas separate.

# Lesson Adaptation for a Teacher or Trainer

A teacher may already have a good lesson but need to adapt it for different session lengths or learner groups.

Property|Value
---|---
**Skill name**|Lesson Adaptation
**Purpose**|Adapt an existing lesson while preserving its learning goals.
**Inputs**|•	Original lesson plan.<br/>•	Learner level.<br/>•	Available time.<br/>•	Available materials.<br/>•	Any accessibility requirements supplied by the teacher.
**Procedure**|1.	Identify the original learning goals.<br/>2.	Keep those goals unless the teacher explicitly changes them.<br/>3.	Shorten or expand activities to fit the new time.<br/>4.	Use only the stated materials.<br/>5.	Include one check for understanding.<br/>6.	Mark any assumption that needs the teacher to confirm it.
**Output**|Revised lesson plan with timing.

*Table 3.4F: Lesson Adaptation skill specification for a Teacher or Trainer.*

> **Sample files**: A completed Lesson Adaptation skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/lesson-adaptation/.

The skill does not need to know everything about teaching. It needs to perform one stable adaptation procedure well.

# Manuscript Consistency Check for a Publisher or Author

Publishing contains many repeated checks that are ideal for skills because the rules are explicit but tedious to repeat.

Property|Value
---|---
**Skill name**|Manuscript Consistency Check
**Purpose**|Review a chapter against a book's style guide and internal cross-reference rules.
**Inputs**|•	Chapter draft.<br/>•	Style guide.<br/>•	List of chapter and section titles.<br/>•	Optional list of product names and preferred terminology.
**Procedure**|1.	Check headings against the chapter structure.<br/>2.	Check figure and table numbering.<br/>3.	Check references to other chapters and sections.<br/>4.	Check product terminology against the preferred-term list.<br/>5.	Flag repeated explanations that might belong elsewhere.<br/>6.	Produce a report of proposed fixes without silently rewriting the manuscript.
**Output**|A prioritized review report.

*Table 3.4G: Manuscript Consistency Check skill specification for a Publisher or Author.*

> **Sample files**: A completed Manuscript Consistency Check skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/manuscript-consistency-check/.

This is a good example of a skill that helps a professional without replacing the professional. The author or editor decides which changes to make.

# Weekly Decision and Action Review for Operations

Operations work often involves gathering loose decisions and follow-up actions from several sources.

Property|Value
---|---
**Skill name**|Decision and Action Review
**Purpose**|Turn approved notes into a consistent list of decisions, owners, deadlines, and unresolved questions.
**Inputs**|•	Meeting notes.<br/>•	Action tracker.<br/>•	Reporting period.
**Procedure**|1.	Extract explicit decisions.<br/>2.	Extract explicit actions, owners, and dates.<br/>3.	Do not invent an owner or deadline.<br/>4.	Mark missing owners or dates.<br/>5.	Merge exact duplicates.<br/>6.	Separate overdue actions from upcoming actions.<br/>7.	End with unresolved questions.
**Output**|A compact weekly operations review.

*Table 3.4H: Weekly Decision and Action Review skill specification for Operations.*

> **Sample files**: A completed Weekly Decision and Action Review skill is here: https://github.com/markjprice/claude-vb/tree/main/Files/Book3/weekly-decision-and-action-review/.

