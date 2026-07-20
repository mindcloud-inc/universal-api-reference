# BASIC: Get all users in project

Retrieves project users from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-users-in-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-users-in-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-all-users-in-project?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "last_seen_at": "2026-05-07T12:00:00.000Z",
          "meta": {},
          "pds_url": "https://example.com",
          "profile": {},
          "status": "string",
          "user_did": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].id` | string |  |
| `data[].last_seen_at` | date |  |
| `data[].meta` | object |  |
| `data[].pds_url` | string |  |
| `data[].profile` | object |  |
| `data[].status` | string |  |
| `data[].user_did` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/user/` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-users-in-project.md) for the provider-specific parameters and requirements.

