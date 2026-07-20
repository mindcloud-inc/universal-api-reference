# Routee: Retrieve Whatsapp Campaign history

Retrieves WhatsApp campaign history from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-history?connectionId=$CONNECTION_ID&campaignTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-campaign-history?${params}`, {
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
      "history": [
        [
          {}
        ]
      ],
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history[]` | array<object> |  |
| `history[].date` | string |  |
| `history[].status` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /tracking/campaign/:campaignTrackingId/history` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-whatsapp-campaign-history.md) for the provider-specific parameters and requirements.

