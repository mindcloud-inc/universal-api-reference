# Bulldog-WP: Get numbers

Retrieves phone numbers from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-devices?${params}`, {
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
      "agents": [
        "string"
      ],
      "alias": "string",
      "cancelAt": "2026-05-07T12:00:00.000Z",
      "connector": "string",
      "description": "string",
      "id": "string",
      "phone": "string",
      "status": 1,
      "user": {},
      "version": 1,
      "waba": {},
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<string> |  |
| `alias` | string |  |
| `cancelAt` | date |  |
| `connector` | string |  |
| `description` | string |  |
| `id` | string |  |
| `phone` | string |  |
| `status` | number |  |
| `user` | object |  |
| `version` | number |  |
| `waba` | object |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /devices` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-devices.md) for the provider-specific parameters and requirements.

