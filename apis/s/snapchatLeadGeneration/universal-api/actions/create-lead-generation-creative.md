# Snapchat Lead Generation: Create Lead Generation Creative

Creates a lead generation creative in Snapchat Lead Generation.

```
POST https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-creative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-creative" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adAccountId": "string",
  "creatives": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-lead-generation-creative', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adAccountId": "string",
    "creatives": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adAccountId` | string | yes | The Snapchat Ad Account ID that will own the new lead generation creative. |
| `creatives` | list<object> | yes | An array of creative objects for Snapchat lead generation creatives. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creatives": [
        {
          "creative": {
            "ad_account_id": "string",
            "brand_name": "Ava Chen",
            "created_at": "2026-05-07T12:00:00.000Z",
            "headline": "string",
            "id": "string",
            "name": "Ava Chen",
            "packaging_status": "string",
            "preview_creative_id": "string",
            "review_status": "string",
            "shareable": true,
            "top_snap_crop_position": "string",
            "type": "string",
            "updated_at": "2026-05-07T12:00:00.000Z"
          },
          "sub_request_error_reason": "string",
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
| `creatives[].creative.ad_account_id` | string |  |
| `creatives[].creative.brand_name` | string |  |
| `creatives[].creative.created_at` | date |  |
| `creatives[].creative.headline` | string |  |
| `creatives[].creative.id` | string |  |
| `creatives[].creative.name` | string |  |
| `creatives[].creative.packaging_status` | string |  |
| `creatives[].creative.preview_creative_id` | string |  |
| `creatives[].creative.review_status` | string |  |
| `creatives[].creative.shareable` | boolean |  |
| `creatives[].creative.top_snap_crop_position` | string |  |
| `creatives[].creative.type` | string |  |
| `creatives[].creative.updated_at` | date |  |
| `creatives[].sub_request_error_reason` | string |  |
| `creatives[].sub_request_status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `POST /adaccounts/:adAccountId/creatives` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-generation-creative.md) for the provider-specific parameters and requirements.

