# Search Credentials with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/search`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Search Credentials](https://thehyperstack.com/docs/api-guide/search-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | no | Search term matched against credentials. |
| `page` | body | `number` | yes | The page number for pagination. |
| `page_size` | body | `number` | yes | The number of credentials to return per page. |
