# Get Publication Email Blast with Beehiiv

Retrieves an email blast for a publication from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/email_blasts/:emailBlastId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Publication Email Blast](https://files.buildwithfern.com/https%3A//beehiiv.docs.buildwithfern.com/d0f4c30b8707ec784c673704353550d3fb9e00a41983b8f2e3d852f96d93abdb/assets/beehiiv-API-Specification.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `emailBlastId` | path | `string` | yes | The prefixed ID of the email blast object. |
| `expand[]` | query | `array<string>` | no | Optional list of expandable objects. |
