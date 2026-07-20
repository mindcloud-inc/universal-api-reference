# Check Policy Health with Lakera AI Guardrails

## Endpoint

- **Method:** `POST`
- **Path:** `/policies/health`
- **Base URL:** `https://api.lakera.ai/v2`
- **Official documentation:** [Check Policy Health](https://docs.lakera.ai/api-reference/lakera-api/policies-health/check-policy-health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Lakera project ID whose policy configuration health should be checked. |
