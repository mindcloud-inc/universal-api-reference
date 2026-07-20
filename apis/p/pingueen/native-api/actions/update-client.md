# Update Client with Pingueen

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [Update Client](https://etinet.gitbook.io/pingueen/api-reference/clients/update-an-existing-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_name` | body | `string` | no | Client first name. |
| `ds_phone` | body | `string` | no | Phone number with country code. |
| `ds_surname` | body | `string` | no | Client surname. |
| `email` | body | `string` | no | — |
| `id` | path | `string` | yes | ID of the client to update. |
| `opt_in_status` | body | `number` | no | 0 not requested, 100 pending, 200 accepted. |
