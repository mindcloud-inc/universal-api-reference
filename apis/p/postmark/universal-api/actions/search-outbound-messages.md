# Postmark: Search Outbound Messages

Searches outbound messages in Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/search-outbound-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/search-outbound-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/search-outbound-messages?${params}`, {
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
      "Messages": [
        [
          {}
        ]
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Messages[]` | array<object> |  |
| `Messages[].From` | string |  |
| `Messages[].MessageID` | string |  |
| `Messages[].ReceivedAt` | date |  |
| `Messages[].Recipients[]` | array<string> |  |
| `Messages[].Status` | string |  |
| `Messages[].Subject` | string |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /messages/outbound` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-outbound-messages.md) for the provider-specific parameters and requirements.

