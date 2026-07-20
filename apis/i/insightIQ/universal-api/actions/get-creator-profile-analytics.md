# InsightIQ: Get Creator Profile Analytics

Retrieves creator profile analytics from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-profile-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-profile-analytics?connectionId=$CONNECTION_ID&identifier=string&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-profile-analytics?${params}`, {
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
| `identifier` | string | yes | URL, username, handle, or profile URL to analyze |
| `isPremium` | boolean | no | Premium analytics mode for Twitch only |
| `metricCalculationMethod` | string | no | Metric aggregation method; supports average or median Default: `average`. |
| `workPlatformId` | string | yes | Work platform ID for the profile lookup |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_part_of_creator_list": true,
      "price_explanations": [
        {}
      ],
      "pricing": {},
      "profile": {},
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_part_of_creator_list` | boolean |  |
| `price_explanations` | array<object> |  |
| `pricing` | object |  |
| `profile` | object |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/social/creators/profiles/analytics` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creator-profile-analytics.md) for the provider-specific parameters and requirements.

