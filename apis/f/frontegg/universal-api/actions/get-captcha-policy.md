# Frontegg: Get Captcha Policy

Retrieves the CAPTCHA policy from Frontegg.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-captcha-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-captcha-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-captcha-policy?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "ignoredEmails": [
        "ava@example.com"
      ],
      "minScore": 1,
      "secretKey": "string",
      "siteKey": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `ignoredEmails` | array<string> |  |
| `minScore` | number |  |
| `secretKey` | string |  |
| `siteKey` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/configurations/v1/captcha-policy` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-captcha-policy.md) for the provider-specific parameters and requirements.

