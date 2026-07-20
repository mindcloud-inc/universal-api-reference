# Update Lead with Octanist

Updates an existing lead in Octanist.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/leads`
- **Base URL:** `https://octanist.com/api`
- **Official documentation:** [Update Lead](https://octanist.com/docs/api-reference/endpoint/update-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Lead ID to update. Highest-priority match key. |
| `email` | body | `string` | no | Lead email. Used as the second-priority match key when id is not provided. |
| `phone` | body | `string` | no | Lead phone. Used as the third-priority match key when id and email are not provided. |
| `status` | body | `string` | no | New lead status. |
| `value` | body | `number` | no | Lead value. |
| `note` | body | `string` | no | Note to attach to the lead. |
| `lossReason` | body | `string` | no | Reason for loss when status is lost. |
