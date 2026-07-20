# Delegate Lead with Myphoner

Delegates or claims a lead in Myphoner.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/leads/:leadId/delegate`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Delegate Lead](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delegate_to` | body | `string` | no | User ID or email that should hold the claim of the lead. |
| `leadId` | path | `number` | yes | The Myphoner lead ID. |
