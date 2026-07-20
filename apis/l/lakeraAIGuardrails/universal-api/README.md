# <img src="https://images.mindcloud.co/apps/icons/lakerafavicon_1776113614668.jpeg" alt="Lakera AI Guardrails logo" width="28" height="28"> Lakera AI Guardrails: Universal API

Screen AI interactions for prompt injection, data leakage, and policy violations with Lakera Guard.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lakeraAIGuardrails/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lakera.ai/
- **Vendor API docs:** https://docs.lakera.ai/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Policy Health](actions/check-policy-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Guard Detector Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed Detector Results](actions/get-detailed-detector-results.md) | GET |  |

### Guard Screening Result

| Action | Method | Description |
| --- | --- | --- |
| [Screen Content for Threats](actions/screen-content-for-threats.md) | GET |  |

### Policy Health Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Policy Health](actions/check-policy-health.md) | GET |  |

