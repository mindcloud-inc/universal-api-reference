# TrueMail: Check Usage

Retrieves account usage details from TrueMail.

```
GET https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage?${params}`, {
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
      "credits": {
        "locked": 1,
        "total": 1
      },
      "period": {
        "end": "string",
        "start": "string"
      },
      "plan": "string",
      "rateLimit": {
        "limit": 1
      },
      "validationTypes": {
        "mx": {
          "available": true,
          "credits": 1
        },
        "smtp": {
          "available": true,
          "credits": 1,
          "upgradeRequired": "string"
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
| `credits.locked` | number |  |
| `credits.total` | number |  |
| `period.end` | string |  |
| `period.start` | string |  |
| `plan` | string |  |
| `rateLimit.limit` | number |  |
| `validationTypes.mx.available` | boolean |  |
| `validationTypes.mx.credits` | number |  |
| `validationTypes.smtp.available` | boolean |  |
| `validationTypes.smtp.credits` | number |  |
| `validationTypes.smtp.upgradeRequired` | string |  |

## Native endpoint

Through the native TrueMail API, this operation is `GET /v1/usage` (base URL `https://api.mailcop.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-usage.md) for the provider-specific parameters and requirements.

