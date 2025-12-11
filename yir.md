# Apr 2024 - Mar 2025

## What did you achieve?

- **Summarise your performance relative to the objectives or outcomes you have achieved this financial year.**
- **You need to reference all four Macquarie Objectives.**
- **The Macquarie Objectives are:**
  - **Professional Conduct, DEI, People Leadership (if applicable)**
  - **Business Leadership (including Customer and Community Outcomes)**
  - **Risk Management and Compliance**
  - **Financial / Business Results**

Professional Conduct, Diversity, Equity and Inclusion:

- I consistently uphold Macquarie's Principles of Opportunity, Accountability and Integrity in all aspects of my work both within and beyond the office. I treat all employees with respect, value diverse perspectives, and recognize the unique strengths that each individual brings. This commitment allows me to meaningfully contribute to Macquarie's exceptional culture of inclusion and collaboration.
- I promote institutional knowledge-sharing by creating detailed Confluence documentation and placing thorough updates on the Jira ticket I am working on. This greatly streamlines the collaboration process between developers in our team as it allows them to stay informed about the status of my ticket and to have all the context required in a shared document.
- I am always the first to speak up whenever I don't understand something, to ask for further clarification or to take accountability for my mistakes. I'm always open to taking feedback and advice from others in order to improve. My high levels of transparency in communication and openness to receive feedback has greatly enabled team members to raise any issues/concerns with me and to have detailed discussions on how to improve upon mistakes and what can be learnt from them.

Business Leadership:

- Throughout my work, I have prioritised long term and scalable solutions over tactical fixes by always looking for ways to improve existing systems and methods of practice and to leverage knowledge and best practices from other teams.
- I created a GCP Route Checker tool that allows developers to quickly and easily determine if a deployment would remove any existing routes after a dry-run. The creation of this tool was motivated after a bug in the GCP Platform caused one of our prod deployments to wipe all of our existing routes.
- Whenever I am working with services or apis outside of our team, I will collaborate with engineers from various teams in order to get a better understanding of the service, e.g. Jayeeta's team with the New Borrower Rate Api. This has helped to solve cross-group issues and challenges more effectively.

Risk Management and Compliance

- Having Risk Management and Compliance at the back of my mind along with a fine attention to detail has enabled me to quickly identify, escalate, own and manage both financial and non-financial risks throughout projects that I have worked on.
- The most recent example of this is when I noticed that one of our api's did not have injection for Corelogic's client-secret implemented yet (in a pre-prod readiness call with my lead engineer). This observation allowed us to mitigate the risk of a possible production incident and prevent associated downtime.

Financial/Business Results

- This year I have delivered high quality and meaningful contributions to various projects such as: Creation of GCP Route Checker Tool, Connecting LiabilityMatchingV2 Api to Nucleus ReportingEventApi, Integrate LiabilityMatchingV2Api with NewBorrowerRate Api, Uplift TitleSearch to OpenApiV3, Connecting valuations-ordering-api to QE MockServer, Fastvals feature work on valuations-ordering-api.
- One example of this is how after discovering the lack of client-secret injection in valuations-ordering-api, my lead engineer and I were able to repurpose and reuse previous code that I had written for another microservice and resolve the issue within just 1-2 hours of discovery. This demonstrates the high quality, reusability, and well-documented nature of my work, which facilitated quick adaptation and resolution in a time-sensitive situation.

## How did you demonstrate cultural/behavioural expectations?

- **Summarise how you demonstrated the principles of the Macquarie Code of Conduct and the three Macquarie Standards in the performance and delivery of your objectives.**
- **The Macquarie Standards are:**
  - **Deliver our Purpose**
  - **Develop Myself and Others**
  - **Manage Risk.**
- **The Macquarie Code of Conduct are: Opportunity, Accountability, Integrity (Our Code of Conduct sets out our purpose, our principles and guides us on how we are expected to behave. It equips us to manage risks, make good decisions, speak up with our ideas and concerns, listen to others, be effective supervisors and understand our policy requirements.)**

Deliver our Purpose: I take accountability for my work by delivering and achieving results on time. I proactively reach out to key stakeholders both internally within my team and externally outside my team whenever I need clarification or assistance. I build trust with team members through my high levels of communication and transparency. I consider both the near and long-term impacts of my work by making high quality contributions and writing detailed documentation.

Develop Myself and Others: I deeply value the opportunity to be part of Macquarie's team by embracing diverse perspectives, respecting and learning from the contributions of others. I am committed to personal growth by actively pursuing new challenges, maintaining an open mindset, and seeking constructive feedback to continuously improve. I contribute to Macquarie's team by creating detailed Confluence documentation to share my learnings and to promote institutional knowledge-sharing. I regularly take time for self-reflection to evaluate and to identify areas of improvement.

Manage Risk: I act with honesty and integrity. I proactively identify, escalate and manage risks. I have the courage to take accountability for my mistakes and to speak up whenever I encounter uncertainty or observe something that doesn't seem right. I make risk informed decisions by taking into account diverse perspectives from team members. During high-pressure situations I am able to remain calm, focused and am capable of making sound judgments.

# Apr 2025 - Mar 2026

## 2025 Q1 (1st April - 4th July)

For Q1 2025, I have been actively working to "expand my T" to transition from a junior engineer to an emerging engineer by deepening my expertise across multiple apis (LiabilityMatchingV2, ValuationsOrderingApi, IncomeVerificationV2) and broadening my knowledge on multiple domains (e.g. root cause analysis using the tools available to us i.e. SumoLogic, Dynatrace).

Most of my time this quarter has been working on the Income Verification Uplift Epic which involves a major upgrade to the IncomeVerificationApi to enable it to consume payslip data from Documatic (GenAi). Throughout this epic work, I have taken ownership of the implementation of the more complex feature work that are medium to large size. With advisory guidance from senior engineers, I have independently implemented

- Migration of Karate Test Automation framework into Domain Api
- Cross Project PubSub Publisher and Subscriber functionality to multiple topics
- The application_state and document_cache databases (and corresponding logic) for applications and documents
- Cron job (scheduler) to timeout applications that have not received a GenAi response within a configurable SLA period
- A bypass mechanism to turn off sending and receiving of data from Documatic (GenAi)

I have also greatly utilised the AI tools available to us such as Vertex Ai, RooCode

- Generating dashboards on both SumoLogic and Dynatrace for key metrics
- Speed up development by generating boilerplate code and generating tests to ensure high code coverage
- Migration of Spanner emulators from an external repository into domain api (this proved to be incredibly helpful because I was able to fix an issue with the Spanner emulator when one day the latest tagged Docker image broke our Bitbucket pipelines)
- Combining the Spanner Emulators and PubSub Emulators into a single class which allows both Spanner Database and PubSub Topics & Subscriptions to be simultaneously created and used for integration and automation tests
- Finding areas for optimisation after implementation (such as reducing the number of database calls from N to 1)
  - findAllById

I actively communicate concisely, effectively and clearly with my team on the status of my progress, seek clarification and support whenever something is unclear or blocks my progress. One example of such was at the start of the epic in communicating to Jihang about the complexities faced with testing the Cross Project PubSub Publisher and Subscriber functionality using emulators which required his help to debug. I consistently spend time to create and maintain relevant documentation to promote knowledge sharing between engineers (insert-link-here) and have been generous with my time in helping new engineers to onboard onto the project by helping them debug issues faced. Another example is in the discussions I had with Ajit regarding the cache implementation logic and approaching his suggestions with an open mind which in turn allowed for a stronger solution of the cache implementation logic by having cache reconciliation (between request and response) as well as the untying of application_id from the document_cache table.

I have been proactive in using my learnings both from past epic work on Valuations and the current epic work on Income to observe and suggest improvements to engineering practices in order to deliver reliable and quality solutions. One example of such is my message to notify of the issues with the Documatic contracts in #initiative especially in regards to the major lack of engineering practices (lack of contract versioning and communication about changes, contract not being placed in Bitbucket, removal of Request and Response contracts from Confluence page, renaming of key fields in the new contract that would cause breaking changes to adopt) and of issues that IV2 will have of consuming other types of documents such as rental income. (insert-link-here)

Outside of my work on the Income Verification Uplift Epic

- I have gained exposure and experience in utilising SumoLogic and Dynatrace to investigate and perform root cause analysis on production issues raised in the BTSD tickets. I am particularly proud of my "Support Issues Register" documentation that I maintained during my time on Support for FY26.Q1.S3 sprint which has been used as a template by other engineers on subsequent support roster rotations.
- Documented detailed preparation of how to perform the rotation of aceeventpegabpm GA accounts
- Spent time to create and maintain existing repositories of knowledge via shared Confluences
  - Created a Prod Release Implementation Plan Template that aims to consolidate all required information regarding a prod release for an api
  - Created Roo Code Guide and Vertex Ai Guide (with sample prompts) documentations to share tips and tricks I have found in using these Ai tools
  - Created a Dynatrace and SumoLogic Query Templates
  - Created a bunch more documentation under the Integration Dev Space Page in the DLO Confluence space

## 2025 Q2 (4th July - 10th September)

For Q2 2025, I have been actively working to "expand my T" to transition from a junior engineer to an emerging engineer by deepening my expertise of the steps required for a successful production release through delivery of the IncomeVerificationV2 Uplift Epic (to Consume Payslips from GenAi) to production and broadening my knowledge of the tools used for observability during highcare period.

Most of my time this quarter has been working on delivering/deploying the Income Verification Uplift Epic to production and utilising all available tools i.e. SumoLogic, Dynatrace to implement observability for the release.

I have taken ownership of the implementation of:

- Configurable Environment value “pubsubConversationId” that prevents deployed and local instances of IncomeVerificationV2 Api from concurrently writing to cache.
  - This is done through sending the pubsubConversationId value as the mglConversationId value in the header of IV2’s GenAi request.
  - IV2 then verifies the returned value of the mglConversationId header in the GenAi response matches the configured pubsubConversationId environment value. If there is no match, then the message is ignored.
  - This implementation also doubly serves as a safety mechanism to allow IV2 to gracefully ignore any messages from GenAi that were not requested by itself
- Creation of Sumologic and Dynatrace Dashboards in both non-prod and prod that captures
  - Number of Incoming ACE Requests to IV2
  - Number of Invalid mglConversationId in GenAi Response
  - Number of JsonProcessingException in GenAi Response
  - Number and Percentage of Request Timeouts to GenAi
  - Number of Unknown Flagged Substring Occurrences in GenAi Response
  - The following are in table format capturing the latencies: average, 50th, 75th, 90th, 95th, 99th percentiles
    - IV Response Time
    - GenAi Response Time
    - GenAi Response Times Breaching SLA > 10 minutes (Timeout)
    - SpannerDB Cache Document Retrieval Time
  - SpannerDB Cache Utilisation Rate
  - IV2 Domian Async Response Ratios: Success (IV00SC), Error (IV00E), BypassDocumatic (IV00SAI)
  - Number of Publishing Calls to GenAi
- Adding OTEL Trace Spans into IncomeVerificationV2 Api
  - This has been one of the most useful additions to IncomeVerificationV2 Api as it allows for Sumologic Alerts to be triggered in non-prod, the injection of custom key value pairs that allow Slack alert messages to be overhauled to provide useful information such as: dynamic urls to trace span page, mgl-correlation-id, application-id
  - Please refer to the following confluence page INSERT_HERE
- HighCare KT Handover Docs
- Actively Maintained HighCare Alert Docs of GenAi Request Timeout
- Documatic Contract Discussion Confluence with Steve
  - Breaking changes with new contract
- Maintained IV2 Asset Page
- Created docs
  - Venafi Cert Decom Steps
  - GA Decommission Steps
- Sumlogic log search to assist in finding GenAi requests that never receive a GenAi response

## 2025 Q3 (10th September - 3rd November)

Actively participated in knowledge upskilling workshops

- Philip DeGrasso Ngyuen’s Incident Management Workshop (Monday 29th September)
- Temporal Skills Development Training (Monday 13th October)

Presented

- Using OTEL Trance Spans in our alerts (Tuesday 4th November)

## Technical Craft & Execution

- This pillar is about the quality of your engineering work.
- Think about: designing scalable systems, writing robust code, and demonstrating deep technical knowledge.
- L2
  - Think about a time you had to understand how your code changes would interact with adjacent components, or when you effectively used debugging tools to resolve bugs.
- L3
  - Think about a time you participated in the design of new features, solved a non-trivial technical challenge, or balanced an ideal solution with business needs and delivery timelines.
- L4
  - Think about how you demonstrated deep understanding and ownership of one or more core systems, or a time you made a key decision balancing ideal solutions with delivery timelines.

Key Contributions & Accomplishments:

Throughout the Income Verification Uplift Epic (involving major upgrades to the IncomeVerificationApi to enable consumption of payslip data from Documatic), I have taken ownership of the implementation of the more complex feature work that are medium to large size. With advisory guidance from senior engineers, I have independently implemented

- Dual PubSub Publisher and Subscriber functionality to publish and subscribe to multiple topics across multiple GCP projects: DLO & Data Science (the first DLO microservice to achieve this functionality)
  - This allows IncomeVerificationApi to asynchronously: send payslip document extraction requests to Documatic, process payslip document data returned from Documatic, return consolidated response to ACE
- Creation of SpannerDB Cache that stores payslip document data returned from Documatic
  - This reduces IV domain operation cost by skipping extraction request calls to Documatic for documents that have already been processed within 90 days and improves the IV api response time for all application re-submission requests
- Migration of Karate Test Automation framework into Domain Api
  - This allows automation tests to be run against IncomeVerificationApi both locally and as a part of our pipelines. This has greatly helped in ensuring code changes do not break existing functionality and has sped up development work as developers no longer need to deploy their changes in order to run automation tests.
- Fail safety mechanisms such as: a bypass mechanism to turn off sending and receiving of data from Documatic and a cron job (scheduler) that utilises the SpannerDB Cache to continuously monitor payslip document extraction requests sent to Documatic and timing out requests that have not received a Documatic response within a configurable SLA period. The associated pubsub message that is sent back to ACE in the event of an extraction request timeout allows the ACE workflow to continue

Examples of times when I had solved solved a non-trivial technical challenge

- Configurable Environment value “pubsubConversationId” that prevents deployed and local instances of IncomeVerificationV2 Api from concurrently writing to cache.

## Project Delivery & Ownership:

- L2
  - Think about a feature request you broke down into actionable steps, or a time you identified the root cause of an issue, not just the symptoms.
- L3
  - Think about a significant component or feature set you took ownership of from design to deployment, or a complex production issue you investigated and resolved.
- L4
  - Think about a time you took part in technical discussions and influenced outcomes within your team, or stepped into a tech lead role for a smaller initiative.

Key Contributions & Accomplishments:

A significant component or feature set you took ownership of from design to deployment was the implementation of the observability side of Income Verification such as integration of OTEL Trace Spans into IncomeVerificationApi and the creation of Sumologic and Dynatrace Dashboards in both non-prod and prod

- This has greatly increased the observability and monitoring of IncomeVerificationApi as it allows for Sumologic Alerts to be triggered in non-prod environments whilst engineers are developing features and ensuring that the correct alerts are triggered for specific error scenarios
- The creation of IncomeVerificationApi alerts based on OTEL Trace Spans allowed the uplift of Slack alert messages to provide useful and actionable information such as: what, why, error type, trace-id and dynamic urls that open to the Sumologic trace span page through the implementation of custom key value pairs on each error span.
- The IncomeVerificationApi dashboards that captures key metrics such as: number and Percentage of Request Timeouts to GenAi, p50/p90/p99 percentiles of Documatic response time, Async Response Ratios has been integral in capturing how key integration points especially those with Documatic perform during performance testing and has helped to identify latency issues and incidents related to Documatic

## Collaboration & Communication

- This pillar is about your impact on others.
- Think about: mentoring, code reviews, documentation, and working effectively with non-technical stakeholders.
- L2
  - Collaboration & Communication: Think about how you contributed to the team's code quality through thoughtful code reviews and well-tested solutions.
- L3
  - Collaboration & Communication: Think about a time you clearly articulated technical concepts to team members, or provided guidance and support to more junior engineers.
- L4
  - Collaboration & Communication: Think about how you provided robust technical mentorship and coaching, or effectively collaborated with product managers and designers.
- Robust technical mentorship and coaching,
  - HighCare KT Handover Docs
  - Actively Maintained HighCare Alert Docs of GenAi Request Timeout
  - Documatic Contract Discussion Confluence with Steve
    - Breaking changes with new contract
  - Created docs
    - Venafi Cert Decom Steps
    - GA Decommission Steps
- Gave a presentation on “Using OTEL Trance Spans in our alerts” at DLO Engineering Team Meeting

## Strategic Impact & Growth

- This pillar is about thinking bigger than your immediate task.
- Think about: driving long-term improvements, reducing tech debt, and connecting your work to business goals.
- L2
  - Think about how you have consistently demonstrated a growth mindset, perhaps by proactively looking for bigger challenges.
- L3
  - Think about a discussion you contributed to about technical debt or identified areas for improvement within the team.
- L4
  - Think about the long-term implications of your technical decisions, or a time you suggested a system-level improvement to get prioritized.

Reducing technical debt and reducing KCJ impacts

- Reopened thread leaks PR for ValuationsOrderingApi,
- Debugging alerts with ValuationsOrderingApi timeouts
  - Found root cause due to null pointer exception
  - Found another cause due to limitation of database design
  - Implemented optimistic concurrency locking to prevent dual deployed pods from concurrently updating cache
