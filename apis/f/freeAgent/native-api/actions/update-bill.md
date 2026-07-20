# Update Bill with FreeAgent

Updates an existing bill in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bills/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Bill](https://dev.freeagent.com/docs/bills#update-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent bill ID. |
| `bill` | body | `object` | no | Bill payload. |
| `bill.contact` | body | `string` | no | Contact being billed. |
| `bill.reference` | body | `string` | no | Free-text reference. |
| `bill.dated_on` | body | `date` | no | Date of bill. |
| `bill.due_on` | body | `date` | no | Due date of bill. |
| `bill.currency` | body | `string` | no | Bill currency. |
| `bill.comments` | body | `string` | no | Free-text comments. |
| `bill.project` | body | `string` | no | Project billed for. |
