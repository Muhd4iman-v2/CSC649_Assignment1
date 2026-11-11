# Tech Stack Evaluation

## Project
Computer Vision-Assisted MyJPJ eAduan.

## Requirements that drive the decision
List 3 to 5 requirements from your own docs/requirements.md. Include at
least 2 non-functional requirements.
- [FR1]: [The system shall analyze pictures and videos uploaded by public users to automatically classify the offense category, extract missing report details, and evaluate initial evidence clarity.]
- [FR4]: [The system shall evaluate submitted evidence on an AI server and categorize cases into "Strong Evidence" (flagged as high priority) and "Weak Evidence" (flagged as low priority).]
- [NFR1]: [The system shall analyze uploaded pictures and videos to produce initial offense category suggestions and clarity feedback within 1 minute of submission.]
- [NFR2]: [The system shall process continuous high volumes of public traffic complaints without significant system lag or performance degradation.]
- [NFR5]: [The system shall maintain a precision of at least 80% when declaring the offense confidence score during media evaluation.]

## Options
- Option A: [MyJPJ with JPJ-owned AI server for both initial feedback and deeper AI analysis]
- Option B: [MyJPJ with third-party AI cloud server for both initial feedback and deeper AI analysis]
- Option C: [MyJPJ with Mobile Edge AI for initial feedback and third-party AI cloud server for deeper AI analysis]

## Decision matrix
Weight: how important the criterion is for YOUR project (1 = low, 5 = high).
Score: how well each option does (1 = poor, 5 = excellent).
Weighted score = weight x score. Add them up for each option.

| Criterion                          | Weight | A score | B score | C score |
|------------------------------------|--------|---------|---------|---------|
| Fits my requirements               |   5    |     4   |     4   |     5   |
| Skills I already have              |   4    |     3   |     3   |     4   |
| Time to build before my deadline   |   5    |     1   |     3   |     4   |
| Free hosting and tools             |   2    |     2   |     4   |     4   |
| Performance and security needs     |   5    |     3   |     4   |     5   |
| Room to grow later                 |   3    |     3   |     5   |     5   |
| **Total (weighted)**               |        |    65   |    90   |   109   |

## Decision record
**Context:** The MyJPJ eAduan system faces an accumulating backlog of pending traffic complaints due to slow manual officer reviews and high user submission rates. The system must handle high volumes of user-submitted photos and videos for automated offense classification, clarity feedback, metadata extraction, and priority scoring. The project constraints include tight deadline, current developer skills, budget limitations for cloud compute, and the need to prevent system lag during complaint surges.

**Decision:** Option C: MyJPJ with Mobile Edge AI for initial feedback and third-party AI cloud server for deeper AI analysis

**Reasons:** 
- Optimized Performance: Using a hybrid approach optimizes both the instant feedback speed expected during the initial submission stage and provides the extra computational resources required for deeper server-side media analysis
-  Scalability: Leveraging a third-party AI cloud server allows JPJ from physical facility constraints, making it significantly easier to scale resources up or down during peak traffic complaint surges in the future.
- Deploying dedicated on-premise infrastructure would delay operational deployment, as setting up and procuring JPJ-owned AI servers from scratch takes considerable time, whereas third-party cloud infrastructure is ready to deploy almost immediately.

**Consequences:** 
- What becomes easy: Public user will receive immediate, responsive UI feedback on their mobile devices, while cloud server compute remains reserved strictly for evaluating clear, strong evidence.
- What becomes hard: Developing, testing, and maintaining two separate AI model pipelines.

**Risks and next review:** 
- what could go wrong: Low-end smartphone hardware may struggle with local Mobile Edge AI inference speed, and utilizing third-party cloud servers may expose citizen traffic evidence to data privacy or security risks.
- Next Review: Benchmark edge model execution speed on budget devices and evaluate cloud security protocols during the initial prototype testing phase.
    
