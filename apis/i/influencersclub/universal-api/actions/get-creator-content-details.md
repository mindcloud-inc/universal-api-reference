# Influencers.club: Get Creator Content Details

Retrieves detailed metrics for specific creator content in Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/get-creator-content-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/get-creator-content-details?connectionId=$CONNECTION_ID&platform=string&contentType=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "string",
  "contentType": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/get-creator-content-details?${params}`, {
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
| `platform` | string | yes | Platform of the content (instagram, tiktok, youtube). |
| `contentType` | string | yes | Content details to fetch (data, comments, transcript, audio). |
| `postId` | string | yes | Target platform post identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paginationToken` | string | no | Token for next comment page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_cost": 1,
      "result": {},
      "trial_searches_left": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_cost` | number | Credits consumed by this request. |
| `result` | object | Detailed content payload for a specific creator post. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/creators/content/details/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creator-content-details.md) for the provider-specific parameters and requirements.

