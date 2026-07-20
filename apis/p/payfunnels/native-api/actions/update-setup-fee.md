# Update Setup Fee with Payfunnels

Updates an existing setup fee in Payfunnels.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/fees/setup/{id}`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Update Setup Fee](https://api.payfunnels.com/api/docs/#update-one-time-setup-fees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the setup fee to update. |
| `name` | body | `string` | no | Updated name for the setup fee. |
| `setAsDefault` | body | `boolean` | no | Set true to mark this setup fee as default for the business. |
