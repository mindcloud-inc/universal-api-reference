# Brevo: Get SMS Campaign



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sms-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sms-campaign?${params}`, {
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
| `campaignId` | number | yes | The SMS campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": 1,
      "name": "Ava Chen",
      "sender": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | The SMS message content. |
| `id` | number | The SMS campaign id. |
| `name` | string | The SMS campaign name. |
| `sender` | string | The SMS sender. |
| `status` | string | The SMS campaign status. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/smsCampaigns/:campaignId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-campaign.md) for the provider-specific parameters and requirements.

