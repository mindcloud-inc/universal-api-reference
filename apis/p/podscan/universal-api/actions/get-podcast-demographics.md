# Podscan: Get Podcast Demographics

Retrieves podcast demographics data from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-demographics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-demographics?connectionId=$CONNECTION_ID&podcast=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "podcast": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-demographics?${params}`, {
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
| `podcast` | string | yes | The podcast ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": "string",
      "age_distribution": [
        {}
      ],
      "age_gender_distribution": [
        {}
      ],
      "brand_relationship": {},
      "content_habits": {},
      "education_level": "string",
      "engagement_level": "string",
      "episodes_analyzed": 1,
      "family_status_distribution": [
        {}
      ],
      "gender_skew": "string",
      "geographic_distribution": [
        {}
      ],
      "ideological_leaning": {},
      "living_environment": {},
      "professional_industry": [
        {}
      ],
      "purchasing_power": "string",
      "technology_adoption": {},
      "total_episodes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string |  |
| `age_distribution` | array<object> |  |
| `age_gender_distribution` | array<object> |  |
| `brand_relationship` | object |  |
| `content_habits` | object |  |
| `education_level` | string |  |
| `engagement_level` | string |  |
| `episodes_analyzed` | number |  |
| `family_status_distribution` | array<object> |  |
| `gender_skew` | string |  |
| `geographic_distribution` | array<object> |  |
| `ideological_leaning` | object |  |
| `living_environment` | object |  |
| `professional_industry` | array<object> |  |
| `purchasing_power` | string |  |
| `technology_adoption` | object |  |
| `total_episodes` | number |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /podcasts/{podcast}/demographics` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-demographics.md) for the provider-specific parameters and requirements.

