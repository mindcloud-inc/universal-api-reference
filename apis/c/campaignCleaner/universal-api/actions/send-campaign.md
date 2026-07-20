# Campaign Cleaner: Send Campaign

Submits a campaign for processing in Campaign Cleaner.

```
POST https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/send-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Cleaner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/send-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "send_campaign.campaign_html": "string",
  "send_campaign.campaign_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/send-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "send_campaign.campaign_html": "string",
    "send_campaign.campaign_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `send_campaign.campaign_html` | string | yes | The full HTML for the campaign to process. |
| `send_campaign.campaign_name` | string | yes | The campaign name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `send_campaign.custom_info` | string | no | Optional metadata to store with the campaign. |
| `send_campaign.webhook_url` | string | no | Optional webhook URL to receive the completed campaign payload. |
| `send_campaign.adjust_font_colors` | boolean | no | Adjust bright font colors that can trigger spam filters. |
| `send_campaign.inline_css` | boolean | no | Inline CSS styles directly into HTML elements. |
| `send_campaign.remove_comments` | boolean | no | Remove CSS and HTML comments. |
| `send_campaign.remove_css_inheritance` | boolean | no | Remove inherited CSS after inlining. |
| `send_campaign.resize_and_host` | boolean | no | Resize and host eligible images on Campaign Cleaner CDN. |
| `send_campaign.remove_image_height` | boolean | no | Remove explicit image heights. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object | Created or processed campaign payload when Campaign Cleaner accepts the submission. |
| `error` | string | Provider-level error message returned even when the HTTP status is 200, for example when the tenant has no remaining credits. |

## Native endpoint

Through the native Campaign Cleaner API, this operation is `POST /v1/send_campaign` (base URL `https://api.campaigncleaner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-campaign.md) for the provider-specific parameters and requirements.

