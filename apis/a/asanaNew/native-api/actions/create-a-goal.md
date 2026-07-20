# Create a goal with Asana

Creates a goal in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a goal](https://developers.asana.com/reference/creategoal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
