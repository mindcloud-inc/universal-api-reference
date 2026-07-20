# Deep Infra: List Account Email Values



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-account-email-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-account-email-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-account-email-values?${params}`, {
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
      "email": "ava@example.com",
      "primary": true,
      "status": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Account email value. |
| `primary` | boolean | Whether this is the primary email address. |
| `status` | string | Email verification or account status. |
| `verified` | boolean | Whether the email value is verified. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/me/emails` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-email-values.md) for the provider-specific parameters and requirements.

