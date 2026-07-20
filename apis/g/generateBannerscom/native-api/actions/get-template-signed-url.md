# Get Template Signed URL with GenerateBanners.com

Retrieves a signed render URL for a GenerateBanners.com template.

## Endpoint

- **Method:** `GET`
- **Path:** `/{publicApiKey}/template/:id/sign-url`
- **Base URL:** `https://api.generatebanners.com/api/v1`
- **Official documentation:** [Get Template Signed URL](https://www.generatebanners.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the template to generate a signed render URL for. |
