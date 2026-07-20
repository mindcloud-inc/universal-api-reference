# Add Lead with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Add Lead](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Street address for the lead when using parsed address input. |
| `address2` | body | `string` | no | Optional second address line when using parsed address input. |
| `city` | body | `string` | no | City for the lead when using parsed address input. |
| `state` | body | `string` | no | State for the lead when using parsed address input. |
| `zip` | body | `string` | no | ZIP code for the lead when using parsed address input. |
| `latitude` | body | `number` | no | Latitude for the lead when using coordinate input. |
| `longitude` | body | `number` | no | Longitude for the lead when using coordinate input. |
| `full_address` | body | `string` | no | Single-string full address for the lead when using full-address input. |
