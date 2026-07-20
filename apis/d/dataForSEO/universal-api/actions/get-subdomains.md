# DataForSEO: Get Subdomains

Retrieves subdomain data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-subdomains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-subdomains?connectionId=$CONNECTION_ID&limit=25&offset=0&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "target": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-subdomains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target` | string | yes | Domain to analyze for subdomains. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |
| `ignore_synonyms` | boolean | no | Exclude synonymous keywords from the subdomain analysis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": {},
      "seType": "string",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics` | object | Keyword and traffic metrics for the returned subdomain. |
| `seType` | string | Search engine type for the subdomain record. |
| `subdomain` | string | Subdomain returned for the requested target. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/subdomains/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subdomains.md) for the provider-specific parameters and requirements.

