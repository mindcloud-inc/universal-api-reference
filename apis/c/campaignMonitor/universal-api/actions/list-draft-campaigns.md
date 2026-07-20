# Campaign Monitor: List Draft Campaigns

Retrieves draft campaigns for a Campaign Monitor client.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-draft-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-draft-campaigns?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-draft-campaigns?${params}`, {
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
| `clientId` | string | yes | Campaign Monitor client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "dateCreated": "string",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "name": "Ava Chen",
      "previewTextUrl": "https://example.com",
      "previewUrl": "https://example.com",
      "replyTo": "string",
      "subject": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Campaign Monitor campaign identifier. |
| `dateCreated` | string | Date the draft campaign was created. |
| `fromEmail` | string | Sender email address for the draft campaign. |
| `fromName` | string | Sender name for the draft campaign. |
| `name` | string | Draft campaign name. |
| `previewTextUrl` | string | Hosted plain-text preview URL for the draft campaign. |
| `previewUrl` | string | Hosted preview URL for the draft campaign. |
| `replyTo` | string | Reply-to email address for the draft campaign. |
| `subject` | string | Draft campaign subject line. |
| `tags` | array<string> | Tags associated with the draft campaign. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /clients/:clientId/drafts.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-draft-campaigns.md) for the provider-specific parameters and requirements.

