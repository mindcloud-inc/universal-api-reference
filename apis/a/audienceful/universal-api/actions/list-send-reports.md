# Audienceful: List Send Reports

Retrieves a list of send reports from Audienceful.

```
GET https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-send-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-send-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-send-reports?${params}`, {
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
| `search` | string | no | Search send reports that match the provided string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audiences": [
        "string"
      ],
      "completedAt": "2026-05-07T12:00:00.000Z",
      "draft": {},
      "id": "string",
      "identity": "string",
      "stats": {},
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audiences` | array<string> | Audiences targeted by the send. |
| `completedAt` | date | UTC timestamp when the send completed. |
| `draft` | object | Draft metadata for the email that was sent. |
| `id` | string | Audienceful send report ID. |
| `identity` | string | Identity the email was sent from. |
| `stats` | object | Aggregate delivery, open, click, unsubscribe, complaint, and failure stats. |
| `subject` | string | Email subject for the send report. |

## Native endpoint

Through the native Audienceful API, this operation is `GET /emails/reports` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-send-reports.md) for the provider-specific parameters and requirements.

