# Delete Contact with Paycove

Deletes a contact from Paycove.

## Endpoint

- **Method:** `DELETE`
- **Path:** `contacts/:id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Delete Contact](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Paycove CRMContact ID. |
| `delete_subscriptions` | query | `boolean` | no | Delete subscriptions associated with this contact. |
