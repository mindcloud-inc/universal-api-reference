# Submit parallel requests with Asana

Submits parallel API requests to Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `batch`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Submit parallel requests](https://developers.asana.com/reference/createbatchrequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.actions[]` | body | `array` | yes | — |
| `data.actions[].data` | body | `object` | yes | — |
| `data.actions[].method` | body | `string` | yes | — |
| `data.actions[].options.fields` | body | `list` | yes | — |
| `data.actions[].options.limit` | body | `number` | yes | — |
| `data.actions[].options.offset` | body | `number` | yes | — |
| `data.actions[].relative_path` | body | `string` | yes | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.actions` | body | `list<string>` | no | Asana actions parameter. |
