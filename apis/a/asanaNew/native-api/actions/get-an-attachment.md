# Get an attachment with Asana

Retrieves an attachment from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `attachments/:attachment_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get an attachment](https://developers.asana.com/reference/getattachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_gid` | path | `string` | yes | Asana attachment gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
