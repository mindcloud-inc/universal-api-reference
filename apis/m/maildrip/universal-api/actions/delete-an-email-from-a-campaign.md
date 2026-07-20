# Maildrip: Delete an email from a campaign



```
DELETE https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-email-from-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-email-from-a-campaign?connectionId=$CONNECTION_ID&campaignId=string&campaignEmailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "campaignEmailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-email-from-a-campaign?${params}`, {
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
| `campaignEmailId` | string | yes | ID of the email associated with the campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `DELETE /api/v1/campaigns/{campaignId}/{campaignEmailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-an-email-from-a-campaign.md) for the provider-specific parameters and requirements.

