# Coresignal: Preview Base Jobs By DSL

Previews base jobs in Coresignal from an Elasticsearch DSL query.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-base-jobs-by-dsl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-base-jobs-by-dsl?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/preview-base-jobs-by-dsl?${params}`, {
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
| `query` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "country": "string",
      "created": "string",
      "employment_type": "string",
      "id": 1,
      "location": "string",
      "seniority": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `country` | string |  |
| `created` | string |  |
| `employment_type` | string |  |
| `id` | number |  |
| `location` | string |  |
| `seniority` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `POST /job_base/search/es_dsl/preview` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-base-jobs-by-dsl.md) for the provider-specific parameters and requirements.

