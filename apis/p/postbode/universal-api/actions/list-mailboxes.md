# Postbode: List Mailboxes

Retrieves available mailboxes from the Postbode API.

```
GET https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postbode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes?${params}`, {
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
      "available_balance": 1,
      "balance": 1,
      "id": 1,
      "name": "Ava Chen",
      "vat_shifted": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_balance` | number |  |
| `balance` | number |  |
| `id` | number |  |
| `name` | string |  |
| `vat_shifted` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Postbode API, this operation is `GET /mailbox` (base URL `https://app.postbode.nu/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

