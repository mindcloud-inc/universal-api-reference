# Curator: Create Ad

Creates an ad or custom post in Curator.

```
POST https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-ad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedId": "string",
  "networkId": 1,
  "name": "Ava Chen",
  "positionStart": 1,
  "positionRepeats": true,
  "text": "string",
  "status": "string",
  "clickAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedId": "string",
    "networkId": 1,
    "name": "Ava Chen",
    "positionStart": 1,
    "positionRepeats": true,
    "text": "string",
    "status": "string",
    "clickAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedId` | string | yes | Feed to assign the ad to. |
| `networkId` | number | yes | Network identifier for the ad. |
| `name` | string | yes | Ad name. |
| `positionStart` | number | yes | Starting position for the ad. |
| `positionRepeats` | boolean | yes | Whether the ad repeats. |
| `positionRepeatInterval` | number | no | Repeat interval when repeating is enabled. |
| `text` | string | yes | Ad text. |
| `status` | string | yes | Ad status. |
| `clickAction` | string | yes | Behavior when the ad is clicked. |
| `url` | string | no | Target URL when click action is goto-url. |
| `imageUrl` | string | no | Optional external image URL. |
| `videoUrl` | string | no | Optional external video URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickAction": "string",
      "feedId": "string",
      "id": "string",
      "name": "Ava Chen",
      "networkId": 1,
      "networkName": "Ava Chen",
      "positionRepeatInterval": 1,
      "positionRepeats": true,
      "positionStart": 1,
      "slug": "string",
      "status": "string",
      "text": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickAction` | string |  |
| `feedId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `networkId` | number |  |
| `networkName` | string |  |
| `positionRepeatInterval` | number |  |
| `positionRepeats` | boolean |  |
| `positionStart` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `text` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Curator API, this operation is `POST /v1.2/ads` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ad.md) for the provider-specific parameters and requirements.

