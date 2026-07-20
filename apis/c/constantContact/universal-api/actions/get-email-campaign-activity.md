# Constant Contact: Get Email Campaign Activity

Retrieves an email campaign activity from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-activity?connectionId=$CONNECTION_ID&campaignActivityId=91569d46-00e4-4a4d-9a4c-d17d98740d04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignActivityId": "91569d46-00e4-4a4d-9a4c-d17d98740d04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-email-campaign-activity?${params}`, {
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
| `campaignActivityId` | string | yes | The unique ID for an email campaign activity. Example: `91569d46-00e4-4a4d-9a4c-d17d98740d04`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated additional fields to include. Example: `html_content,permalink_url`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignActivityId": "string",
      "campaignId": "string",
      "contactListIds": [
        "string"
      ],
      "currentStatus": "string",
      "formatType": 1,
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "replyToEmail": "ava@example.com",
      "role": "string",
      "segmentIds": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignActivityId` | string |  |
| `campaignId` | string |  |
| `contactListIds` | array |  |
| `currentStatus` | string |  |
| `formatType` | number |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `replyToEmail` | string |  |
| `role` | string |  |
| `segmentIds` | array |  |
| `subject` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /emails/activities/:campaign_activity_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign-activity.md) for the provider-specific parameters and requirements.

