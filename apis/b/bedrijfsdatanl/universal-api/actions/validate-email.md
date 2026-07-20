# Bedrijfsdata.nl: Validate Email



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-email?${params}`, {
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
| `email` | string | no | Email address to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "email": {
        "disposable": 1,
        "domain": "ava@example.com",
        "email": "ava@example.com",
        "free": 1,
        "mxHost": "ava@example.com",
        "mxIp": "ava@example.com",
        "success": 1,
        "user": "ava@example.com",
        "wrongEmail": 1,
        "wrongFormat": 1
      },
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `email.disposable` | number |  |
| `email.domain` | string |  |
| `email.email` | string |  |
| `email.free` | number |  |
| `email.mxHost` | string |  |
| `email.mxIp` | string |  |
| `email.success` | number |  |
| `email.user` | string |  |
| `email.wrongEmail` | number |  |
| `email.wrongFormat` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /email` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

