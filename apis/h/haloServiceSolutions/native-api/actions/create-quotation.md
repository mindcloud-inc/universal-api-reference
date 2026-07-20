# Create Quotation with Halo Service Solutions

Creates a new quotation in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotation`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Quotation](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `[].title` | body | `string` | no |
| `[].client_id` | body | `number` | no |
| `[].user_id` | body | `number` | no |
| `[].agent_id` | body | `number` | no |
| `[].site_id` | body | `number` | no |
| `[].ticket_id` | body | `number` | no |
| `[].date` | body | `date` | no |
| `[].expiry_date` | body | `date` | no |
| `[].note` | body | `string` | no |
