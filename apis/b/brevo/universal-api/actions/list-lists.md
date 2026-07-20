# Brevo: List Lists



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists?${params}`, {
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
      "count": 1,
      "lists": [
        {
          "folderId": 1,
          "id": 1,
          "name": "Ava Chen",
          "totalBlacklisted": 1,
          "totalSubscribers": 1,
          "uniqueSubscribers": 1
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
| `count` | number |  |
| `lists[].folderId` | number |  |
| `lists[].id` | number |  |
| `lists[].name` | string |  |
| `lists[].totalBlacklisted` | number |  |
| `lists[].totalSubscribers` | number |  |
| `lists[].uniqueSubscribers` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/lists` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

