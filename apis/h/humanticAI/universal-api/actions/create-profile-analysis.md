# Humantic AI: Create Profile Analysis



```
POST https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-profile-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humantic AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-profile-analysis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-profile-analysis', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | LinkedIn profile URL, email address, or another unique identifier for the individual being analyzed. Do not use values starting with `test`. |
| `firstname` | string | no | Optional first name. Helpful when the identifier is an email address. |
| `lastname` | string | no | Optional last name. Helpful when the identifier is an email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enrichprofile` | boolean | no | For eligible plans and email identifiers, controls whether Humantic tries to resolve associated social profile data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "results": {
        "userid": "string",
        "username": "Ava Chen"
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
| `results.userid` | string |  |
| `results.username` | string |  |
| `status` | string |  |
| `usage_stats.user_profile.consumed` | number |  |
| `usage_stats.user_profile.limit` | number |  |
| `usage_stats.user_profile.remaining` | number |  |
| `usage_stats.user_profile.subscription_status` | string |  |

## Native endpoint

Through the native Humantic AI API, this operation is `GET /user-profile/create` (base URL `https://api.humantic.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-profile-analysis.md) for the provider-specific parameters and requirements.

