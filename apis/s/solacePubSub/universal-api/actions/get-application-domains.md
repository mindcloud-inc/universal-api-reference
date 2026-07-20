# Solace PubSub+: Get Application Domains

Retrieves application domains from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-application-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-application-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-application-domains?${params}`, {
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
      "changedBy": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "deletionProtected": true,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "stats": {},
      "type": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedBy` | string |  |
| `createdBy` | string |  |
| `createdTime` | date |  |
| `deletionProtected` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `stats` | object |  |
| `type` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/architecture/applicationDomains` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-application-domains.md) for the provider-specific parameters and requirements.

