# List Signature History with edatalia Sign Online

Retrieves signature history from edatalia Sign Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/PSC/v40/History`
- **Base URL:** `https://restapi.firmar.online`
- **Official documentation:** [List Signature History](https://restapi.firmar.online/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Limit` | query | `number` | no | Maximum number of history items to return. Provider maximum is 100. |
| `Offset` | query | `number` | no | Number of history items to skip. |
| `Reference` | query | `string` | no | Filter history by envelope reference. |
| `DocumentSetName` | query | `string` | no | Filter history by envelope name. |
| `RecipientEmail` | query | `string` | no | Filter history by recipient email. |
| `OnlyCurrentUser` | query | `boolean` | no | When true, only return envelopes for the current authenticated user. |
