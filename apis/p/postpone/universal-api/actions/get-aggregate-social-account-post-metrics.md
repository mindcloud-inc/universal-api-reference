# Postpone: Get Aggregate Social Account Post Metrics

Retrieves aggregate social account post metrics from Postpone.

```
GET https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-social-account-post-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-social-account-post-metrics?connectionId=$CONNECTION_ID&variables.startDate=string&variables.endDate=string&variables.socialAccountIds%5B%5D=string&variables.metrics%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.startDate": "string",
  "variables.endDate": "string",
  "variables.socialAccountIds[]": "string",
  "variables.metrics[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-social-account-post-metrics?${params}`, {
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
| `variables.startDate` | string | yes |  |
| `variables.endDate` | string | yes |  |
| `variables.socialAccountIds[]` | array<string> | yes |  |
| `variables.metrics[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": [
        {
          "aggregation": "string",
          "metric": "string",
          "value": 1
        }
      ],
      "socialAccount": {
        "avatarUrl": "https://example.com",
        "formattedUsername": "Ava Chen",
        "id": "string",
        "platform": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics[].aggregation` | string |  |
| `metrics[].metric` | string |  |
| `metrics[].value` | number |  |
| `socialAccount.avatarUrl` | string |  |
| `socialAccount.formattedUsername` | string |  |
| `socialAccount.id` | string |  |
| `socialAccount.platform` | string |  |
| `socialAccount.username` | string |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregate-social-account-post-metrics.md) for the provider-specific parameters and requirements.

