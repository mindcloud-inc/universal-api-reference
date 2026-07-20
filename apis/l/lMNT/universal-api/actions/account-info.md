# LMNT: Account Info

Retrieves your account details from LMNT.

```
GET https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LMNT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info?${params}`, {
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
      "plan": {
        "character_limit": 1,
        "commercial_use_allowed": true,
        "professional_voice_limit": 1,
        "type": "string"
      },
      "usage": {
        "characters": 1,
        "credit_characters": 1,
        "instant_voices": 1,
        "period_end": 1,
        "professional_voices": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plan` | object |  |
| `plan.character_limit` | number |  |
| `plan.commercial_use_allowed` | boolean |  |
| `plan.professional_voice_limit` | number |  |
| `plan.type` | string |  |
| `usage` | object |  |
| `usage.characters` | number |  |
| `usage.credit_characters` | number |  |
| `usage.instant_voices` | number |  |
| `usage.period_end` | number |  |
| `usage.professional_voices` | number |  |

## Native endpoint

Through the native LMNT API, this operation is `GET /v1/account` (base URL `https://api.lmnt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-info.md) for the provider-specific parameters and requirements.

