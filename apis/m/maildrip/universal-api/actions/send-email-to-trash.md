# Maildrip: Send email to trash



```
DELETE https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-to-trash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-to-trash?connectionId=$CONNECTION_ID&campaignId=string&campaignEmailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "campaignEmailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-to-trash?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign |
| `campaignEmailId` | string | yes | ID of the email to be sent to trash |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedEmail": "ava@example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedEmail` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/campaigns/{campaign_id}/{campaign_email_id}/send-mail-to-trash` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-to-trash.md) for the provider-specific parameters and requirements.

