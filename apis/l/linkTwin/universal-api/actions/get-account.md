# LinkTwin: Get Account

Retrieves your account details from LinkTwin.

```
GET https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account?${params}`, {
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
      "currentPlan": "string",
      "email": "ava@example.com",
      "expired": "string",
      "expiryDate": {},
      "limits": {
        "alias": {
          "enabled": "string"
        },
        "clicks": 1,
        "delete": {
          "enabled": "string"
        },
        "domain": {
          "count": 1,
          "enabled": "string"
        },
        "export": {
          "enabled": "string"
        },
        "links": 1,
        "retention": 1,
        "team": {
          "count": 1,
          "enabled": "string"
        }
      },
      "settings": {
        "defaultDomain": "string",
        "timezone": "string",
        "timezoneOffset": 1
      },
      "usage": {
        "clicks": 1,
        "clicksResetDays": 1,
        "links": 1,
        "missedClicks": 1
      },
      "userId": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPlan` | string |  |
| `email` | string |  |
| `expired` | string |  |
| `expiryDate` | object |  |
| `limits.alias.enabled` | string |  |
| `limits.clicks` | number |  |
| `limits.delete.enabled` | string |  |
| `limits.domain.count` | number |  |
| `limits.domain.enabled` | string |  |
| `limits.export.enabled` | string |  |
| `limits.links` | number |  |
| `limits.retention` | number |  |
| `limits.team.count` | number |  |
| `limits.team.enabled` | string |  |
| `settings.defaultDomain` | string |  |
| `settings.timezone` | string |  |
| `settings.timezoneOffset` | number |  |
| `usage.clicks` | number |  |
| `usage.clicksResetDays` | number |  |
| `usage.links` | number |  |
| `usage.missedClicks` | number |  |
| `userId` | number |  |
| `verified` | boolean |  |

## Native endpoint

Through the native LinkTwin API, this operation is `GET /account` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

