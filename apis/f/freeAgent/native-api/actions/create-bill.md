# Create Bill with FreeAgent

Creates a new bill in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/bills`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Bill](https://dev.freeagent.com/docs/bills#create-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bill` | body | `object` | no | Bill payload. |
| `bill.contact` | body | `string` | yes | Contact being billed. |
| `bill.reference` | body | `string` | yes | Free-text reference. |
| `bill.dated_on` | body | `date` | yes | Date of bill. |
| `bill.due_on` | body | `date` | yes | Due date of bill. |
| `bill.currency` | body | `string` | no | Bill currency. |
| `bill.comments` | body | `string` | no | Free-text comments. |
| `bill.project` | body | `string` | no | Project billed for. |
