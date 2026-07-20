# Unkey: Query key verification data

Retrieves key verification data from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/query-key-verification-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/query-key-verification-data?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/query-key-verification-data?${params}`, {
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
| `query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/analytics.getVerifications` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-key-verification-data.md) for the provider-specific parameters and requirements.

