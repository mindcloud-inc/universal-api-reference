# Migrate Lead with Myphoner

Moves a lead to another list in Myphoner.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/leads/:leadId/migrate`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Migrate Lead](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `give_back_leads` | body | `boolean` | no | When true, release the lead if it is currently claimed. |
| `leadId` | path | `number` | yes | The Myphoner lead ID. |
| `to_list_id` | body | `number` | yes | The destination Myphoner list ID. |
