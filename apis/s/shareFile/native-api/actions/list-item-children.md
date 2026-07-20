# List Item Children with ShareFile

## Endpoint

- **Method:** `GET`
- **Path:** `/Items({{id}})/Children`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [List Item Children](https://api.sharefile.com/html/docs/Items.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ShareFile item identifier whose children should be listed. |
