# Meetstream AI: List Google Domains

Retrieves Google domains from Meetstream AI.

```
GET https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-google-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-google-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-google-domains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active_login_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "login_count": 1,
      "login_mode": "string",
      "max_concurrent_per_login": "string",
      "name": "Ava Chen",
      "sso_workspace_domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_login_count` | number |  |
| `created_at` | date |  |
| `login_count` | number |  |
| `login_mode` | string |  |
| `max_concurrent_per_login` | string |  |
| `name` | string |  |
| `sso_workspace_domain` | string |  |

## Native endpoint

Through the native Meetstream AI API, this operation is `GET /google-login-domains` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-domains.md) for the provider-specific parameters and requirements.

