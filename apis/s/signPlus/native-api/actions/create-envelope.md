# Create Envelope with Sign.Plus

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Create Envelope](https://apidoc.sign.plus/api-reference/endpoints/signplus/create-new-envelope)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Envelope name |
| `flow_type` | body | `string` | yes | Envelope flow type |
| `legality_level` | body | `string` | yes | Envelope legality level |
| `expires_at` | body | `number` | no | Unix timestamp for envelope expiration |
