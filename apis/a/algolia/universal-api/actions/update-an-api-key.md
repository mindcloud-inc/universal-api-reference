# Algolia: Update an API Key

Updates an existing API key in Algolia.

```
PUT https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-an-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-an-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "acl[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-an-api-key', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "acl[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | API key to update. |
| `acl[]` | array<string> | yes | Access control list permissions for the API key. |
| `description` | string | no | Description of the API key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validity` | number | no | Duration in seconds before the key expires. |
| `indexes[]` | array<string> | no | Restrict the API key to a set of indices. |
| `maxHitsPerQuery` | number | no | Maximum number of results returned per query. |
| `maxQueriesPerIpPerHour` | number | no | Maximum number of queries per IP address per hour. |
| `queryParameters` | string | no | Search parameters enforced by this API key. |
| `referers[]` | array<string> | no | Restrict the API key to specific HTTP referrers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `PUT /1/keys/:key` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-an-api-key.md) for the provider-specific parameters and requirements.

