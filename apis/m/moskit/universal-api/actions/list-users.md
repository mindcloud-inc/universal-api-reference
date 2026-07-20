# Moskit: List Users

Retrieves users from Moskit.

```
GET https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users?${params}`, {
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
      "active": true,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "jobTitle": "string",
      "levelBulk": true,
      "levelConfig": true,
      "levelDelete": true,
      "levelEdit": "string",
      "levelExport": true,
      "levelView": "string",
      "name": "Ava Chen",
      "phones": [
        [
          {}
        ]
      ],
      "picture": "string",
      "primaryPhone": {
        "id": 1
      },
      "team": {
        "id": 1
      },
      "timezone": {
        "id": 1
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `dateCreated` | date |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `levelBulk` | boolean |  |
| `levelConfig` | boolean |  |
| `levelDelete` | boolean |  |
| `levelEdit` | string |  |
| `levelExport` | boolean |  |
| `levelView` | string |  |
| `name` | string |  |
| `phones[]` | array<object> |  |
| `phones[].id` | number |  |
| `phones[].number` | string |  |
| `picture` | string |  |
| `primaryPhone` | object |  |
| `primaryPhone.id` | number |  |
| `team` | object |  |
| `team.id` | number |  |
| `timezone` | object |  |
| `timezone.id` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Moskit API, this operation is `GET users` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

