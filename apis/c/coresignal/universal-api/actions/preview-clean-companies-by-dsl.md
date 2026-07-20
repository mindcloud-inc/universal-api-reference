# Coresignal: Preview Clean Companies By DSL

Previews clean companies in Coresignal from an Elasticsearch DSL query.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-clean-companies-by-dsl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-clean-companies-by-dsl?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-clean-companies-by-dsl?${params}`, {
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
| `query` | object | yes | Elasticsearch DSL query object for Clean Company preview. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_score": 1,
      "company_name": "Ava Chen",
      "hq_country": "string",
      "id": 1,
      "industry": "string",
      "linkedin_url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_score` | number |  |
| `company_name` | string |  |
| `hq_country` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `linkedin_url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `POST /company_clean/search/es_dsl/preview` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-clean-companies-by-dsl.md) for the provider-specific parameters and requirements.

