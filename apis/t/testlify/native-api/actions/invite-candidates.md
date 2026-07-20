# Invite Candidates with Testlify

Creates candidate invitations in Testlify for an assessment.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/assessment/candidate/invites`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Invite Candidates](https://docs.testlify.com/reference/invite_candidates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assessmentId` | body | `string` | yes | Assessment identifier. |
| `candidateInvites[].email` | body | `string` | yes | Candidate email address. |
| `candidateInvites[].firstName` | body | `string` | yes | Candidate first name. |
| `candidateInvites[].lastName` | body | `string` | yes | Candidate last name. |
| `source` | body | `string` | no | Invitation source label. |
| `metadata.correlationId` | body | `string` | no | Correlation identifier for downstream tracking. |
| `scheduledDate` | body | `date` | no | Scheduled invitation date. |
