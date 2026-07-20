# Starfish: List Accommodations

Retrieves a list of accommodations from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-accommodations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-accommodations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-accommodations?${params}`, {
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
      "accommodationId": 1,
      "accommodationUid": "string",
      "adminId": 1,
      "arrangements": [
        {}
      ],
      "description": "string",
      "id": 1,
      "labels": [
        {}
      ],
      "media": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "rank": 1,
      "services": [
        {}
      ],
      "status": "string",
      "translations": [
        {}
      ],
      "type": "string",
      "vatProcent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accommodationId` | number |  |
| `accommodationUid` | string |  |
| `adminId` | number |  |
| `arrangements` | array<object> |  |
| `description` | string |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `media` | array<object> |  |
| `meta` | object |  |
| `name` | string |  |
| `rank` | number |  |
| `services` | array<object> |  |
| `status` | string |  |
| `translations` | array<object> |  |
| `type` | string |  |
| `vatProcent` | number |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /accommodations` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accommodations.md) for the provider-specific parameters and requirements.

