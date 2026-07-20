# HackMD: List Teams



```
GET https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HackMD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/list-teams?${params}`, {
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
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "path": "string",
      "upgraded": true,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `path` | string |  |
| `upgraded` | boolean |  |
| `visibility` | string |  |

## Native endpoint

Through the native HackMD API, this operation is `GET /teams` (base URL `https://api.hackmd.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

