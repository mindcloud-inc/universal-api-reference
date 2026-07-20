# Sonderplan: Get Calendar Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-calendar-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-calendar-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-calendar-subscriptions?${params}`, {
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
      "bookingProperty": "string",
      "calendarUrl": "https://example.com",
      "enabled": true,
      "id": 1,
      "lastCheckedDate": 1,
      "lastCheckedFilesize": 1,
      "lastParsedDate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingProperty` | string |  |
| `calendarUrl` | string |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `lastCheckedDate` | number |  |
| `lastCheckedFilesize` | number |  |
| `lastParsedDate` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /calendar-subscription/import` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-subscriptions.md) for the provider-specific parameters and requirements.

