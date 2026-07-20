# Maildrip: Get landing page details for a campaign



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-landing-page-details-for-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-landing-page-details-for-a-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-landing-page-details-for-a-campaign?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "alttext": "string",
      "background_color": "string",
      "button": {},
      "form_fields": [
        {}
      ],
      "headline": "string",
      "logo_url": "https://example.com",
      "success_redirect_url": "https://example.com",
      "tagline": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alttext` | string |  |
| `background_color` | string |  |
| `button` | object |  |
| `form_fields` | array<object> |  |
| `headline` | string |  |
| `logo_url` | string |  |
| `success_redirect_url` | string |  |
| `tagline` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaignId}/landing-page` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-landing-page-details-for-a-campaign.md) for the provider-specific parameters and requirements.

