# Influencers.club: Compare Creator Audience Overlap

Retrieves audience overlap metrics for multiple creators in Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/compare-creator-audience-overlap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/compare-creator-audience-overlap?connectionId=$CONNECTION_ID&platform=string&creators%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "string",
  "creators[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/compare-creator-audience-overlap?${params}`, {
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
| `platform` | string | yes | Platform to compare (instagram, tiktok, youtube). |
| `creators[]` | array<string> | yes | Array of 2-10 creator usernames or profile URLs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basics": {},
      "credits_cost": 1,
      "credits_left": 1,
      "details": [
        {}
      ],
      "status": true,
      "success": true,
      "trial_searches_left": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basics` | object | Aggregate overlap summary values. |
| `credits_cost` | number | Credits consumed by this request. |
| `credits_left` | number | Remaining account credits after this request. |
| `details` | array<object> | Per-creator audience overlap details. |
| `status` | boolean | Provider status flag for overlap computation. |
| `success` | boolean | Provider success indicator. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/creators/audience/overlap/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-creator-audience-overlap.md) for the provider-specific parameters and requirements.

