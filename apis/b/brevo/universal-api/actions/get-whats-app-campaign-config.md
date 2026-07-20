# Brevo: Get WhatsApp Campaign Config



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-whats-app-campaign-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-whats-app-campaign-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-whats-app-campaign-config?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "businessStatus": "string",
      "phoneNumberNameStatus": "Ava Chen",
      "phoneNumberQuality": "string",
      "sendingLimit": "string",
      "whatsappBusinessAccountID": 1,
      "whatsappBusinessAccountStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessStatus` | string | The business verification status. |
| `phoneNumberNameStatus` | string | The phone number name status. |
| `phoneNumberQuality` | string | The phone number quality. |
| `sendingLimit` | string | The WhatsApp sending tier. |
| `whatsappBusinessAccountID` | number | The WhatsApp business account id. |
| `whatsappBusinessAccountStatus` | string | The WhatsApp business account status. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/whatsappCampaigns/config` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whats-app-campaign-config.md) for the provider-specific parameters and requirements.

