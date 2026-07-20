# Snapchat Ads: Create Ad Squads

Creates new ad squads in Snapchat Ads.

```
POST https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ad-squads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ad-squads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "adSquads": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ad-squads', {
  method: 'POST',
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
| `campaignId` | string | yes | The Snapchat Campaign ID that will own the ad squads. |
| `adSquads` | list<object> | yes | An array of Snapchat ad squad objects to create. |

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

Through the native Snapchat Ads API, this operation is `POST /campaigns/:campaignId/adsquads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ad-squads.md) for the provider-specific parameters and requirements.

