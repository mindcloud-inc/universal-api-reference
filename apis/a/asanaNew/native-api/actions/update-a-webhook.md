# Update a webhook with Asana

Updates a webhook in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `webhooks/:webhook_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a webhook](https://developers.asana.com/reference/updatewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.filters` | body | `list` | yes | — |
| `webhook_gid` | path | `string` | yes | Asana webhook gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.filters` | body | `list<string>` | no | Asana filters parameter. |
