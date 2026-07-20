# Brevo: Get Email Campaign Shared URL



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign-shared-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign-shared-url?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign-shared-url?${params}`, {
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
| `campaignId` | number | yes | The email campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sharedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sharedUrl` | string | The shared campaign or template URL. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/emailCampaigns/:campaignId/sharedUrl` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign-shared-url.md) for the provider-specific parameters and requirements.

