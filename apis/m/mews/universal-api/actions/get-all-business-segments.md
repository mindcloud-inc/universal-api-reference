# Mews: Get All Business Segments

Retrieves business segments from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-business-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-business-segments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-business-segments?${params}`, {
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
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "serviceId": "string",
      "updatedUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdUtc` | date | Creation timestamp in UTC. |
| `id` | string | Unique identifier of the business segment. |
| `isActive` | boolean | Whether the business segment is active. |
| `name` | string | Business segment name. |
| `serviceId` | string | Service identifier. |
| `updatedUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Mews API, this operation is `POST /businessSegments/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-business-segments.md) for the provider-specific parameters and requirements.

