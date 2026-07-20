# Get Envelope Signing URL with edatalia Sign Online

Retrieves an envelope signing URL from edatalia Sign Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/PSC/v40/DocumentSet/Url/:documentSetId`
- **Base URL:** `https://restapi.firmar.online`
- **Official documentation:** [Get Envelope Signing URL](https://restapi.firmar.online/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentSetId` | path | `string` | yes | Identifier of the envelope whose signing URL should be retrieved. |
