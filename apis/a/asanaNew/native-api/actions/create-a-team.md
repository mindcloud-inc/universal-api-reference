# Create a team with Asana

Creates a team in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `teams`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a team](https://developers.asana.com/reference/createteam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
