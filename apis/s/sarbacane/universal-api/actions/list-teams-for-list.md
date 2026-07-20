# Sarbacane: List Teams for List

Retrieves groups for a list in Sarbacane.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-teams-for-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-teams-for-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-teams-for-list?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Team identifier. |
| `name` | string | Team display name. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /lists/{listId}/teams` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams-for-list.md) for the provider-specific parameters and requirements.

