# BASIC: Get user teams

Retrieves user teams from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-user-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-user-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-user-teams?${params}`, {
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
          "id": "string",
          "name": "Ava Chen",
          "owner": "string",
          "role_name": "Ava Chen",
          "roles": "string",
          "slug": "string"
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
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].owner` | string |  |
| `data[].role_name` | string |  |
| `data[].roles` | string |  |
| `data[].slug` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /team/` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-teams.md) for the provider-specific parameters and requirements.

