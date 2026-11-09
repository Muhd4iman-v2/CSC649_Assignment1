# User Stories

Public Users
1. As a public witness, I want the system to automatically analyze my uploaded photo or video to suggest the offense category and auto-fill missing details, so that I can submit reports quickly without manual entry errors.
- Acceptance Criteria 1:Uploading a photo or video automatically suggests the offense category and pre-fills any missing details.
- Acceptance Criteria 2: The user can review, confirm, or edit auto-filled details before final submission.

2. As a public witness, I want immediate initial feedback on the clarity of my uploaded media within 1 minute, so that I know whether my evidence is sufficient before completing submission.
- Acceptance Criteria 1: The system provides initial evidence clarity feedback within 1 minute of upload.
- Acceptance Criteria 2: If media is evaluated as "Weak Evidence", the user receives an automated notification and prompt to re-upload higher-quality files.

3. As a public witness, I want automated notifications and prompts to re-upload higher-quality media when my evidence is flagged as weak, so that my report doesn't get rejected or stuck indefinitely.
- Acceptance Criteria 1: The system sends an automated notification to the witness when the system flags their submission as "Weak Evidence".
- Acceptance Criteria 2: The notification provides a direct link to a re-upload interface so the witness can submit stronger media without starting a new report.

4. As a public witness, I want an "Others" offense category and a redesigned UI layout, so that I can easily submit traffic violations that do not fit into predefined categories.
- Acceptance Criteria 1: An "Others" offense category is available for unlisted traffic violations.
- Acceptance Criteria 2: The redesigned UI/UX layout guides users step-by-step to minimize submission errors.

5. As a public witness, I want to see how my report is prioritized, so that I understand why certain cases take longer to process and what steps are needed from me.
- Acceptance Criteria 1: The report status screen clearly indicates whether the submission is categorized under "Strong Evidence" or "Weak Evidence".
- Acceptance Criteria 2: The user receives automated status updates as the report progresses to officer review or if additional evidence is requested.

JPJ Officers
1. As a JPJ officer, I want incoming reports automatically categorized into "Strong Evidence" (high priority) and "Weak Evidence" (low priority), so that I can focus my time on high-conviction cases and clear the pending backlog faster.
- Acceptance Criteria 1: Cases flagged as "Strong Evidence" automatically populate at the top of the officer review queue.
- Acceptance Criteria 2: Cases flagged as "Weak Evidence" are assigned low priority until the user provides stronger media.
- Acceptance Criteria 3: The JPJ Officer can still manually access and review "Weak Evidence" cases whenever needed.

2. As a JPJ officer, I want the system to display an AI-generated confidence score alongside the evidence, so that I can make faster and more confident verification decisions.
- Acceptance Criteria 1: The verification screen displays the AI-calculated offense confidence score alongside the uploaded media.
- Acceptance Criteria 2: The AI model maintains a precision target of at least 80% when outputting confidence ratings.

3. As a JPJ officer, I want embedded image/video metadata (timestamps, location, device details) automatically extracted and displayed, so that I can quickly verify evidence authenticity.
- Acceptance Criteria 1: Embedded file metadata (GPS coordinates, capture timestamp, device information) is extracted by the computer vision engine and displayed on the review panel
- Acceptance Criteria 2: Any missing, corrupted, or inconsistent metadata is visually highlighted.

4. As a JPJ officer, I want the computer vision engine to highlight subtle or secondary traffic offenses in the uploaded media, so that no legal violations go unnoticed during manual review.
- Acceptance Criteria 1: The computer vision engine scans media frames to detect and visually flag secondary or unlisted traffic offenses.
- Acceptance Criteria 2: The officer can accept, edit, or dismiss suggested secondary offenses before completing case verification.

5. As a JPJ officer, I want the system to require my explicit manual confirmation before issuing a legal summons or confirming a crime, so that legal enforcement actions remain strictly human-verified.
- Acceptance Criteria 1: The system strictly blocks automated summons issuance or court case creation without explicit officer sign-off.
- Acceptance Criteria 2: The officer's verification action ("Verify and Issue Summons" or "Reject Report") is permanently logged in the JPJ database.