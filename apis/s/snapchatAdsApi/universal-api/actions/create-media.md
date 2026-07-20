# Snapchat Ads: Create Media

Creates new media assets in Snapchat Ads.

```
POST https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adAccountId": "string",
  "media": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/create-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adAccountId": "string",
    "media": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adAccountId` | string | yes | The Snapchat Ad Account ID that will own the media. |
| `media` | list<object> | yes | An array of Snapchat media objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "media": [
        {
          "media": {
            "download_link": "https://example.com",
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
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
| `media[].media.download_link` | string |  |
| `media[].media.id` | string |  |
| `media[].media.name` | string |  |
| `media[].media.type` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/media` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-media.md) for the provider-specific parameters and requirements.

