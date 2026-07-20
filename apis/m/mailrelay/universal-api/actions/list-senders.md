# Mailrelay: List Senders

Retrieves sender profiles from your Mailrelay account.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-senders?${params}`, {
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
      "confirmed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "email": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | boolean |  |
| `createdAt` | date |  |
| `default` | boolean |  |
| `email` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailrelay API, this operation is `GET senders` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-senders.md) for the provider-specific parameters and requirements.

