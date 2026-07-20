# Mailrelay: Bulk Update Subscribers

Updates multiple subscriber records in Mailrelay.

```
PUT https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/bulk-update-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/bulk-update-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulkAction": "remove_from_group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/bulk-update-subscribers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulkAction": "remove_from_group"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allSubscribers` | boolean | no | Update all subscribers instead of a specific list. |
| `bulkAction` | list | yes | Bulk subscriber update action. One of: `0`. Example: `remove_from_group`. |
| `callbackUrl` | string | no | Webhook URL to receive the bulk update task ID when processing finishes. |
| `groupId` | number | no | Group ID used by the bulk update action. Example: `2`. |
| `subscriberIds[]` | array<number> | no | Subscriber IDs affected by the bulk update action. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Mailrelay API, this operation is `PATCH subscribers/bulk_update` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-subscribers.md) for the provider-specific parameters and requirements.

