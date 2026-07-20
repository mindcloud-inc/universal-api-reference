# <img src="https://images.mindcloud.co/apps/icons/verify-tailr-made_1776175532184.png" alt="Verify (Tailr Made) logo" width="28" height="28"> Verify (Tailr Made): Universal API

Analyze resumes for red flags and fraud signals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verifyTailrMade/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tailrmadeai.com/verify-spot-resume-red-flags-before-the-interview-seeksuite/
- **Vendor API docs:** https://tailrmadeai.com/developer-dashboard/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Resume Red Flags](actions/verify-resume-red-flags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifyTailrMade/latest/actions/verify-resume-red-flags?connectionId=$CONNECTION_ID&resumeText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Verify Resume Red Flags](actions/verify-resume-red-flags.md) | GET | Analyzes resume text for red flags in Verify. |

