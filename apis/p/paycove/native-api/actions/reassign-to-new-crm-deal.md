# Reassign To New CRM Deal with Paycove

Updates a Paycove deal with a new CRM deal ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `deals/:id/update-crm-deal-id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Reassign To New CRM Deal](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crm_deal_id` | body | `string` | yes | New CRM deal id to assign. |
| `id` | path | `string` | yes | Paycove deal id. |
