# Maildrip: Preview contacts in segment for campaign



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-contacts-in-segment-for-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-contacts-in-segment-for-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/preview-contacts-in-segment-for-campaign?${params}`, {
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
      "previewContacts": [
        "string"
      ],
      "segment": {},
      "totalContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `previewContacts` | array<string> |  |
| `segment` | object |  |
| `totalContacts` | number |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaignId}/segment/preview` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-contacts-in-segment-for-campaign.md) for the provider-specific parameters and requirements.

