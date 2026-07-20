# Algolia: Create an API Key

Creates a new API key in Algolia.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-an-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-an-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "acl[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-an-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "acl[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acl[]` | array<string> | yes | Permissions this API key can use. |
| `description` | string | no | Description to help identify this API key. |
| `validity` | number | no | Duration in seconds before the API key expires. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexes[]` | array<string> | no | Index names or patterns this API key can access. |
| `maxHitsPerQuery` | number | no | Maximum number of results this key can retrieve in one query. |
| `maxQueriesPerIpPerHour` | number | no | Maximum number of API requests allowed per IP per hour. |
| `queryParameters` | string | no | Query parameters to append when this key is used. |
| `referers[]` | array<string> | no | Allowed HTTP referrers for this API key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | RFC 3339 timestamp when the API key was created. |
| `key` | string | The generated API key. |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/keys` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-an-api-key.md) for the provider-specific parameters and requirements.

