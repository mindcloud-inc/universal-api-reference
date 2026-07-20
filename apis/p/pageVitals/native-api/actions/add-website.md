# Add Website with PageVitals

## Endpoint

- **Method:** `POST`
- **Path:** `/account/websites`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Add Website](https://pagevitals.com/docs/rest-api/reference/websites/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain of the website, without https:// and paths. |
| `displayName` | body | `string` | no | Optional displayed name for the website in the admin UI. |
