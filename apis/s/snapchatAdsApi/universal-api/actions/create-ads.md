# Snapchat Ads: Create Ads

Creates new ads in Snapchat Ads.

```
POST https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adSquadId": "string",
  "ads": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-ads', {
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
| `adSquadId` | string | yes | The Snapchat Ad Squad ID that will own the ads. |
| `ads` | list<object> | yes | An array of Snapchat ad objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {
          "ad": {
            "id": "string",
            "name": "Ava Chen",
            "review_status": "string",
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
| `ads[].ad.id` | string |  |
| `ads[].ad.name` | string |  |
| `ads[].ad.review_status` | string |  |
| `ads[].ad.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adsquads/:adSquadId/ads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ads.md) for the provider-specific parameters and requirements.

