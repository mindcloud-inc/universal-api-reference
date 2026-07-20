# List SMS Senders with Instasent

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project/channel/sms/sender`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [List SMS Senders](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
