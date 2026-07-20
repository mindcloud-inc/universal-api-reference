# Buttondown: Update Subscriber

Updates an existing subscriber in Buttondown.

```
PUT https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id_or_email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id_or_email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id_or_email` | string | yes | Subscriber ID or email address. |
| `email_address` | string | no | Updated subscriber email address. |
| `notes` | string | no | Private notes attached to the subscriber. |
| `tags[]` | array<string> | no | Tags to replace on the subscriber. |
| `type` | list | no | Updated subscriber type. One of: `gifted`, `regular`, `unpaid`, `unsubscribed`. |
| `commenting_disabled` | boolean | no | Whether commenting is disabled for the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickedCount": 1,
      "clickRate": 1,
      "commentingDisabled": true,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deliveredCount": 1,
      "emailAddress": "ava@example.com",
      "emailTransitions": [
        {}
      ],
      "firewallReasons": [
        "string"
      ],
      "id": "string",
      "ipAddress": "string",
      "metadata": {},
      "notes": "string",
      "openCount": 1,
      "openRate": 1,
      "riskScore": 1,
      "source": "string",
      "tags": [
        "string"
      ],
      "transitions": [
        {}
      ],
      "type": "string",
      "unsubscriptionDate": "2026-05-07T12:00:00.000Z",
      "unsubscriptionReason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickedCount` | number | Total click count when available. |
| `clickRate` | number | Click rate when available. |
| `commentingDisabled` | boolean | Whether commenting is disabled for the subscriber. |
| `creationDate` | date | When the subscriber record was created. |
| `deliveredCount` | number | Total delivered email count when available. |
| `emailAddress` | string | Subscriber email address. |
| `emailTransitions` | array<object> | Email transition history for the subscriber. |
| `firewallReasons` | array<string> | Firewall reasons recorded for the subscriber. |
| `id` | string | Buttondown subscriber ID. |
| `ipAddress` | string | Stored subscriber IP address. |
| `metadata` | object | Structured metadata stored on the subscriber. |
| `notes` | string | Internal notes stored on the subscriber. |
| `openCount` | number | Total open count when available. |
| `openRate` | number | Open rate when available. |
| `riskScore` | number | Buttondown firewall risk score when available. |
| `source` | string | How the subscriber entered Buttondown. |
| `tags` | array<string> | Current tags on the subscriber. |
| `transitions` | array<object> | Lifecycle transitions recorded for the subscriber. |
| `type` | string | Current Buttondown subscriber type. |
| `unsubscriptionDate` | date | When the subscriber unsubscribed, if applicable. |
| `unsubscriptionReason` | string | Stored unsubscription reason, if any. |

## Native endpoint

Through the native Buttondown API, this operation is `PATCH /subscribers/:id_or_email` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

