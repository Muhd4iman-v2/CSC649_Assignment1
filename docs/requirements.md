# Requirements

## Functional requirements (what the system must DO)
1. FR1: The system shall analyze pictures and videos uploaded by public users to automatically classify the offense category, extract missing report details, and evaluate initial evidence clarity.
2. FR2: The system shall evaluate submitted evidence on an AI server and categorize cases into "Strong Evidence" (flagged as high priority) and "Weak Evidence" (flagged as low priority)
3. FR3: The system shall provide immediate feedback to public witnesses regarding evidence quality and automatically prompt users to re-upload stronger evidence when their report is flagged as low priority.
4. FR4: The system shall perform deep media analysis on strong evidences to generate an offense confidence score, extract embedded file metadata, and detect subtle or secondary unidentified traffic offenses to assist JPJ officer decision-making.
5. FR5: The system shall require explicit verification by a JPJ officer before confirming a violation or issuing a legal summons.
6. FR6: The system shall provide an "Others" offense category for unlisted violations and incorporate a redesigned UI/UX layout to guide users and reduce submission errors.

## Non-functional requirements (how the system must PERFORM)
1. NFR1: The system shall analyze uploaded pictures and videos to produce initial offense category suggestions and clarity feedback within 1 minute of submission.
2. NFR2: The system shall process continuous high volumes of public traffic complaints without significant system lag or performance degradation.
3. NFR3: The system shall minimize human-induced errors caused by incorrect category selection or mismatched report details through automated visual verification and intuitive UI/UX workflows.
4. NFR4: The system shall consistently and reliably extract embedded metadata across supported image and video formats without data corruption.
5. NFR5: The system shall maintain a precision of at least 80% when declaring the offense confidence score during media evaluation.
