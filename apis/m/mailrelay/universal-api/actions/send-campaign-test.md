# Mailrelay: Send Campaign Test

Sends a Mailrelay campaign to test email addresses.

```
POST https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "testEmails": "apps@mindcloud.co,qa@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "testEmails": "apps@mindcloud.co,qa@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Mailrelay campaign ID. Example: `1`. |
| `testEmails` | string | yes | Comma-separated email addresses for the campaign test send. Example: `apps@mindcloud.co,qa@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailrelay API returns.

## Native endpoint

Through the native Mailrelay API, this operation is `POST campaigns/:id/send_test` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-campaign-test.md) for the provider-specific parameters and requirements.

