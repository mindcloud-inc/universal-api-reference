# <img src="https://images.mindcloud.co/apps/icons/testfuse_1775666000398.jpeg" alt="Testfuse logo" width="28" height="28"> Testfuse: Universal API

AI-powered pre-employment assessment platform for creating assessment specs, managing assessments, and inviting candidates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/testfuse/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://testfuse.com
- **Vendor API docs:** https://api.testfuse.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assessment Specs](actions/list-assessment-specs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Assessment

| Action | Method | Description |
| --- | --- | --- |
| [List Assessment Specs](actions/list-assessment-specs.md) | GET | Retrieves assessment specs available in Testfuse. |
| [List Assessments](actions/list-assessments.md) | GET | Retrieves assessments from Testfuse by assessment spec. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Invite Candidates](actions/invite-candidates.md) | POST | Invites candidates to a Testfuse assessment spec. |

