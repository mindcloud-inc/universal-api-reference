# Braintrust: List Organizations

Retrieves organizations from Braintrust.

```
GET https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintrust `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": {},
      "created": "string",
      "id": "string",
      "imageRenderingMode": {},
      "isDataplanePrivate": {},
      "isUniversalApi": {},
      "name": "Ava Chen",
      "proxyUrl": {},
      "realtimeUrl": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | object |  |
| `created` | string |  |
| `id` | string |  |
| `imageRenderingMode` | object |  |
| `isDataplanePrivate` | object |  |
| `isUniversalApi` | object |  |
| `name` | string |  |
| `proxyUrl` | object |  |
| `realtimeUrl` | object |  |

## Native endpoint

Through the native Braintrust API, this operation is `GET /v1/organization` (base URL `https://api.braintrust.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

