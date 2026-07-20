# Octadesk: List Ticket Groups

Retrieves ticket groups from Octadesk.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-ticket-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-ticket-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-ticket-groups?${params}`, {
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
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Octadesk API, this operation is `GET /tickets/groups` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-groups.md) for the provider-specific parameters and requirements.

