# List SignRequests with SignRequest

## Endpoint

- **Method:** `GET`
- **Path:** `/signrequests/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [List SignRequests](https://signrequest.com/api/v1/docs/#operation/signrequests_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `who` | query | `list<string>` | no | `m`: only me, `mo`: me and others, `o`: only others. Accepted values: `m`, `mo`, `o`. |
| `from_email` | query | `string` | no | Maximum length: 255. |
