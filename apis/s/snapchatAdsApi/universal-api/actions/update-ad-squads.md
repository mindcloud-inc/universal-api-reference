# Snapchat Ads: Update Ad Squads

Updates existing ad squads in Snapchat Ads.

```
PUT https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-squads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-squads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "adSquads": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/update-ad-squads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "adSquads": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The Snapchat Campaign ID that owns the ad squads to update. |
| `adSquads` | list<object> | yes | An array of full Snapchat ad squad objects to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adsquads": [
        {
          "adsquad": {
            "id": "string",
            "name": "Ava Chen",
            "status": "string"
          }
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
| `adsquads[].adsquad.id` | string |  |
| `adsquads[].adsquad.name` | string |  |
| `adsquads[].adsquad.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `PUT /campaigns/:campaignId/adsquads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ad-squads.md) for the provider-specific parameters and requirements.

