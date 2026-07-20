# Humantic AI: Fetch Analysis



```
GET https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humantic AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis?${params}`, {
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
| `id` | string | yes | The same identifier used when the analysis was created. |
| `persona` | string | no | Optional persona context. Humantic documents `sales` and `hiring`; multiple values can be comma-delimited. Accepts multiple values in one string, delimited by `,`. Example: `sales,hiring`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `override` | boolean | no | When true, Humantic may return results for text input under 300 words; docs warn the results may be inaccurate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "metadata": {
        "analysis_status": "string",
        "analysis_type": "string",
        "confidence": {
          "level": "string",
          "score": 1
        },
        "s3_analysis_status": "string",
        "status": "string",
        "status_code": 1
      },
      "results": {
        "persona": {
          "hiring": {
            "profile_url": "https://example.com"
          },
          "sales": {
            "profile_url": "https://example.com"
          }
        },
        "user_id": "string"
      },
      "status": "string",
      "usage_stats": {
        "user_profile": {
          "consumed": 1,
          "limit": 1,
          "remaining": 1,
          "subscription_status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `metadata.analysis_status` | string |  |
| `metadata.analysis_type` | string |  |
| `metadata.confidence.level` | string |  |
| `metadata.confidence.score` | number |  |
| `metadata.s3_analysis_status` | string |  |
| `metadata.status` | string |  |
| `metadata.status_code` | number |  |
| `results.persona.hiring.profile_url` | string |  |
| `results.persona.sales.profile_url` | string |  |
| `results.user_id` | string |  |
| `status` | string |  |
| `usage_stats.user_profile.consumed` | number |  |
| `usage_stats.user_profile.limit` | number |  |
| `usage_stats.user_profile.remaining` | number |  |
| `usage_stats.user_profile.subscription_status` | string |  |

## Native endpoint

Through the native Humantic AI API, this operation is `GET /user-profile/` (base URL `https://api.humantic.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-analysis.md) for the provider-specific parameters and requirements.

