# Create Assessment with CodeSubmit

## Endpoint

- **Method:** `POST`
- **Path:** `/api/external/tests`
- **Base URL:** `https://app.codesubmit.io`
- **Official documentation:** [Create Assessment](https://www.codesubmit.io/integrations/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Assessment description |
| `fork_id` | body | `string` | no | Fork identifier |
| `name` | body | `string` | no | Assessment name |
| `role` | body | `string` | no | Assessment role or track |
| `slug` | body | `string` | no | Assessment slug |
| `template_id` | body | `string` | no | Template identifier |
| `template_meta` | body | `string` | no | Template metadata |
