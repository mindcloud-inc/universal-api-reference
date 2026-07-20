# <img src="https://images.mindcloud.co/apps/icons/testlify_1775665881513.png" alt="Testlify logo" width="28" height="28"> Testlify: Universal API

Create assessments, invite candidates, and review hiring results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/testlify/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://testlify.com
- **Vendor API docs:** https://docs.testlify.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assessments](actions/list-assessments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | POST | Creates a new access token in Testlify. |
| [List Access Tokens](actions/list-access-tokens.md) | GET | Retrieves Testlify access tokens with optional filters. |

### Assessment

| Action | Method | Description |
| --- | --- | --- |
| [Create Assessment From Template](actions/create-assessment-from-template.md) | POST | Creates a Testlify assessment from an existing template. |
| [Create Compose Assessment](actions/create-compose-assessment.md) | POST | Creates a custom assessment in Testlify from scratch. |
| [Get Assessment](actions/get-assessment.md) | GET | Retrieves a specific assessment from Testlify by ID. |
| [List Assessments](actions/list-assessments.md) | GET | Retrieves assessments from Testlify with optional filters and pagination. |
| [List Candidate Assessments](actions/list-candidate-assessments.md) | GET | Retrieves assessments associated with a specific Testlify candidate. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [List Assessment Candidates](actions/list-assessment-candidates.md) | GET | Retrieves candidates for a specific Testlify assessment. |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves candidates from Testlify with optional filters and pagination. |

### Candidate Invite

| Action | Method | Description |
| --- | --- | --- |
| [Invite Candidates](actions/invite-candidates.md) | POST | Creates candidate invitations in Testlify for an assessment. |

### Candidate Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate Result](actions/get-candidate-result.md) | GET | Retrieves a candidate's assessment result from Testlify. |

### Coding Language

| Action | Method | Description |
| --- | --- | --- |
| [List Coding Languages](actions/list-coding-languages.md) | GET | Retrieves available coding languages from Testlify. |

### Industry Type

| Action | Method | Description |
| --- | --- | --- |
| [List Industry Types](actions/list-industry-types.md) | GET | Retrieves available industry types from Testlify. |

### Job Role

| Action | Method | Description |
| --- | --- | --- |
| [List Job Roles](actions/list-job-roles.md) | GET | Retrieves job roles from the Testlify workspace. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Question](actions/get-question.md) | GET | Retrieves a specific question from Testlify by ID. |
| [List Questions](actions/list-questions.md) | GET | Retrieves Testlify questions with optional filters and pagination. |

### Test Library

| Action | Method | Description |
| --- | --- | --- |
| [List Test Libraries](actions/list-test-libraries.md) | GET | Retrieves Testlify test libraries with optional filters and pagination. |

### Test Library Type

| Action | Method | Description |
| --- | --- | --- |
| [List Test Library Types](actions/list-test-library-types.md) | GET | Retrieves available test library types from Testlify. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook subscription in Testlify. |

### Workspace User

| Action | Method | Description |
| --- | --- | --- |
| [Invite Workspace Users](actions/invite-workspace-users.md) | POST | Creates workspace user invitations in Testlify. |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from Testlify with optional filters and pagination. |

