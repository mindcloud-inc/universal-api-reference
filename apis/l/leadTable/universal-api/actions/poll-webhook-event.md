# LeadTable: Poll webhook event



```
GET https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/poll-webhook-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/poll-webhook-event?connectionId=$CONNECTION_ID&campaignID=string&topic=Change%20status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignID": "string",
  "topic": "Change status"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/poll-webhook-event?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignID` | string | yes | The campaign or table used for the webhook sample event. |
| `topic` | list | yes | Webhook topic to poll. One of: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | Webhook sample events returned by LeadTable. |

## Native endpoint

Through the native LeadTable API, this operation is `GET /pollWebhook/{campaignID}/{topic}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poll-webhook-event.md) for the provider-specific parameters and requirements.

