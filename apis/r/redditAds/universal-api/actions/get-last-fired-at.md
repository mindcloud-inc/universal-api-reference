# Reddit Lead Ads: Get Last Fired At

Retrieves the last fired time for a Reddit pixel.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-last-fired-at
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-last-fired-at?connectionId=$CONNECTION_ID&pixelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pixelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-last-fired-at?${params}`, {
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
| `pixelId` | string | yes | Reddit Ads pixel identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastFiredAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastFiredAt` | date | Most recent pixel fire timestamp. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /pixels/{pixel_id}/last_fired_at` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-fired-at.md) for the provider-specific parameters and requirements.

