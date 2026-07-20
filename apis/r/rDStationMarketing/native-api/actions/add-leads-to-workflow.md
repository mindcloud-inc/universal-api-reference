# Add Leads to Workflow with RD Station Marketing

## Endpoint

- **Method:** `POST`
- **Path:** `/platform/workflows/:id/leads`
- **Base URL:** `https://api.rd.services`
- **Official documentation:** [Add Leads to Workflow](https://developers.rdstation.com/reference/post_platform-workflows-id-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Workflow ID in path. |
| `leads[]` | body | `array<string>` | yes | Lista de leads para enviar ao workflow. |
