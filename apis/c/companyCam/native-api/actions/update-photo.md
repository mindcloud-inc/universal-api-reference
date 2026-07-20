# Update Photo with CompanyCam

## Endpoint

- **Method:** `PUT`
- **Path:** `photos/:id`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Update Photo](https://docs.companycam.com/reference/updatephotodescription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the Photo |
| `photo.internal` | body | `boolean` | no | Format: `toggle`. |
| `photo` | body | `object` | no | — |
