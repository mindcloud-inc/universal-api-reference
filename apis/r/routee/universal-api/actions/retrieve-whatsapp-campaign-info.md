# Routee: Retrieve Whatsapp Campaign info

Retrieves WhatsApp campaign info from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-info?connectionId=$CONNECTION_ID&campaignTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-info?${params}`, {
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
| `campaignTrackingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "from": "string",
      "message": {
        "text": "string"
      },
      "to": "string",
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `from` | string |  |
| `message` | object |  |
| `message.text` | string |  |
| `to` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /tracking/campaign/:campaignTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-whatsapp-campaign-info.md) for the provider-specific parameters and requirements.

