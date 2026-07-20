# Search Images with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `api/v3/images/search/{{integration}}.json`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Search Images](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integration` | path | `string` | yes | Image provider slug such as Giphy or Pexels. |
| `search` | query | `string` | yes | Search term for the image provider. |
