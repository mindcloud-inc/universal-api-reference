# Remove Funding Source with Dwolla

Soft deletes a funding source from Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/funding-sources/[:id]`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Remove Funding Source](https://developers.dwolla.com/docs/api-reference/funding-sources/update-or-remove-a-funding-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla funding source ID. |
