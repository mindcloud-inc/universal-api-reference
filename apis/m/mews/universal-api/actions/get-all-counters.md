# Mews: Get All Counters

Retrieves counters from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-counters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-counters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-counters?${params}`, {
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
      "enterpriseId": "string",
      "format": "string",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedUtc": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdUtc` | date | Creation timestamp in UTC. |
| `enterpriseId` | string | Enterprise identifier. |
| `format` | string | Counter formatting template. |
| `id` | string | Unique identifier of the counter. |
| `isDefault` | boolean | Whether this is the default counter. |
| `name` | string | Counter name. |
| `type` | string | Counter type. |
| `updatedUtc` | date | Last update timestamp in UTC. |
| `value` | number | Current counter value. |

## Native endpoint

Through the native Mews API, this operation is `POST /counters/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-counters.md) for the provider-specific parameters and requirements.

