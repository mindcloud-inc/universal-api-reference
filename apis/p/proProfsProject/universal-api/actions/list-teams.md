# ProProfs Project: List Teams

Retrieves a list of teams from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-teams?${params}`, {
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
          "color": "string",
          "teamId": "string",
          "teamName": "Ava Chen",
          "users": [
            {
              "userId": "string",
              "userName": "Ava Chen"
            }
          ]
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
| `data[].color` | string |  |
| `data[].teamId` | string |  |
| `data[].teamName` | string |  |
| `data[].users[].userId` | string |  |
| `data[].users[].userName` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /teams` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

