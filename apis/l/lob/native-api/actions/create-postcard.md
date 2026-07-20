# Create Postcard with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/postcards`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Create Postcard](https://docs.lob.com/#tag/Postcards/operation/postcard_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the postcard job. |
| `to` | body | `string` | yes | Recipient address ID. |
| `from` | body | `string` | yes | Sender address ID or inline US address. |
| `front` | body | `string` | yes | Front artwork for the postcard. |
| `back` | body | `string` | yes | Back artwork for the postcard. |
| `use_type` | body | `string` | yes | Declared mail use type. |
