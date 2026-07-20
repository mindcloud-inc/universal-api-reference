# Add Tags to Photo with CompanyCam

## Endpoint

- **Method:** `POST`
- **Path:** `photos/:id/tags`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add Tags to Photo](https://docs.companycam.com/reference/listphototags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `tags` | body | `list<string>` | no | Send multiple values as a array. |
