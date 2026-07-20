# Routee: Retrieve Viber Single Message by Tracking Id

Retrieves Viber single message by tracking id from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-viber-single-message-by-tracking-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-viber-single-message-by-tracking-id?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-viber-single-message-by-tracking-id?${params}`, {
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
| `trackingId` | string | yes | The tracking Id of the Viber single message. |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve, default value is 20. |
| `sort` | number | no | The field name that will be used to sort the results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "country": "string",
      "direction": "string",
      "expireOnDelivery": true,
      "from": "string",
      "message": "string",
      "originatingService": "string",
      "price": 1,
      "sessionMessage": true,
      "status": {
        "date": "string",
        "reason": {
          "description": "string",
          "detailedStatus": "string"
        },
        "status": "string"
      },
      "to": "string",
      "trackingId": "string",
      "ttl": "string",
      "viberVideo": {
        "duration": 1,
        "fileSize": 1,
        "videoThumbnail": "string",
        "videoUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `country` | string |  |
| `direction` | string |  |
| `expireOnDelivery` | boolean |  |
| `from` | string |  |
| `message` | string |  |
| `originatingService` | string |  |
| `price` | number |  |
| `sessionMessage` | boolean |  |
| `status` | object |  |
| `status.date` | string |  |
| `status.reason` | object |  |
| `status.reason.description` | string |  |
| `status.reason.detailedStatus` | string |  |
| `status.status` | string |  |
| `to` | string |  |
| `trackingId` | string |  |
| `ttl` | string |  |
| `viberVideo` | object |  |
| `viberVideo.duration` | number |  |
| `viberVideo.fileSize` | number |  |
| `viberVideo.videoThumbnail` | string |  |
| `viberVideo.videoUrl` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /viber/tracking/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-viber-single-message-by-tracking-id.md) for the provider-specific parameters and requirements.

