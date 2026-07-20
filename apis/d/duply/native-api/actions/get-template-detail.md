# Get Template Detail with Duply

Retrieves details for a Duply template.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/:templateId`
- **Base URL:** `https://gen.duply.co/v1`
- **Official documentation:** [Get Template Detail](https://app.duply.co/docs#get-template-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | The ID of the template to fetch. |
| `variantName` | query | `string` | no | Optional template variant name. Defaults to the oldest variant when omitted. |
