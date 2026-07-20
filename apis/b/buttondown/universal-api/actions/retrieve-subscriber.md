# Buttondown: Retrieve Subscriber

Retrieves a subscriber from Buttondown by ID or email address.

```
GET https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-subscriber?connectionId=$CONNECTION_ID&id_or_email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id_or_email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-subscriber?${params}`, {
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
| `id_or_email` | string | yes | Subscriber ID or email address. |

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

Through the native Buttondown API, this operation is `GET /subscribers/:id_or_email` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscriber.md) for the provider-specific parameters and requirements.

