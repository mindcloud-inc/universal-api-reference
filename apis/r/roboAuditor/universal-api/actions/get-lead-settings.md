# RoboAuditor: Get Lead Settings



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-settings?${params}`, {
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
      "add_emailalert": 1,
      "alert_emails": [
        "ava@example.com"
      ],
      "block_domains": [
        "string"
      ],
      "block_emails": [
        "ava@example.com"
      ],
      "email_address": 1,
      "email_domain": 1,
      "never_bounce": 1,
      "never_bounce_limit": 1,
      "whitelist_radio": 1,
      "whitelist_urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_emailalert` | number |  |
| `alert_emails` | array<string> |  |
| `block_domains` | array<string> |  |
| `block_emails` | array<string> |  |
| `email_address` | number |  |
| `email_domain` | number |  |
| `never_bounce` | number |  |
| `never_bounce_limit` | number |  |
| `whitelist_radio` | number |  |
| `whitelist_urls` | array<string> |  |

## Native endpoint

Through the native RoboAuditor API, this operation is `GET /lead-settings` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-settings.md) for the provider-specific parameters and requirements.

