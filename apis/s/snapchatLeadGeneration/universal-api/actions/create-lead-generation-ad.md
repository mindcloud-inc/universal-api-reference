# Snapchat Lead Generation: Create Lead Generation Ad

Creates a lead generation ad in Snapchat Lead Generation.

```
POST https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-ad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adSquadId": "string",
  "ads": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adSquadId": "string",
    "ads": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adSquadId` | string | yes | The Snapchat Ad Squad ID that will own the new lead generation ad. |
| `ads` | list<object> | yes | An array of ad objects for Snapchat lead generation ads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {
          "ad": {
            "ad_squad_id": "string",
            "approval_type": "string",
            "creative_id": "string",
            "delivery_status": [
              "string"
            ],
            "effective_status": "string",
            "id": "string",
            "name": "Ava Chen",
            "render_type": "string",
            "review_status": "string",
            "status": "string",
            "type": "string"
          },
          "sub_request_status": "string"
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads[].ad.ad_squad_id` | string |  |
| `ads[].ad.approval_type` | string |  |
| `ads[].ad.creative_id` | string |  |
| `ads[].ad.delivery_status[]` | string |  |
| `ads[].ad.effective_status` | string |  |
| `ads[].ad.id` | string |  |
| `ads[].ad.name` | string |  |
| `ads[].ad.render_type` | string |  |
| `ads[].ad.review_status` | string |  |
| `ads[].ad.status` | string |  |
| `ads[].ad.type` | string |  |
| `ads[].sub_request_status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `POST /adsquads/:adSquadId/ads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-generation-ad.md) for the provider-specific parameters and requirements.

