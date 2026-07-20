# Autom: Get Usage

Retrieves usage details from Autom.

```
GET https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage?${params}`, {
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
      "account": {
        "name": "Ava Chen",
        "slug": "string"
      },
      "apiKey": {
        "active": true,
        "alias": "string",
        "category": {},
        "expires": {},
        "quotas": {
          "daily": {},
          "monthly": {},
          "total": {},
          "weekly": {}
        }
      },
      "credits": {
        "consumed": 1,
        "given": 1,
        "percentUsed": 1,
        "remaining": "string"
      },
      "period": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "rateLimit": {
        "perMinute": {},
        "perSecond": {}
      },
      "remaining": "string",
      "renewalDate": "2026-05-07T12:00:00.000Z",
      "subscription": {
        "percentUsed": 1,
        "remaining": "string",
        "total": 1,
        "used": 1
      },
      "totalUsed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.name` | string |  |
| `account.slug` | string |  |
| `apiKey.active` | boolean |  |
| `apiKey.alias` | string |  |
| `apiKey.category` | object |  |
| `apiKey.expires` | object |  |
| `apiKey.quotas.daily` | object |  |
| `apiKey.quotas.monthly` | object |  |
| `apiKey.quotas.total` | object |  |
| `apiKey.quotas.weekly` | object |  |
| `credits.consumed` | number |  |
| `credits.given` | number |  |
| `credits.percentUsed` | number |  |
| `credits.remaining` | string |  |
| `period.end` | date |  |
| `period.start` | date |  |
| `rateLimit.perMinute` | object |  |
| `rateLimit.perSecond` | object |  |
| `remaining` | string |  |
| `renewalDate` | date |  |
| `subscription.percentUsed` | number |  |
| `subscription.remaining` | string |  |
| `subscription.total` | number |  |
| `subscription.used` | number |  |
| `totalUsed` | number |  |

## Native endpoint

Through the native Autom API, this operation is `GET /usage` (base URL `https://api.autom.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

