# Template creation with Routee

Creates a new template in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/template`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Template creation](https://docs.routee.net/reference/template-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The name of the template (the parameter is optional, if not specified, the name will be displayed as Template YYYY.mm.dd H:i:s) |
| `body` | body | `string` | yes | HTML version of the email, encoded in base64 |
