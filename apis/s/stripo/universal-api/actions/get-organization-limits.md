# Stripo: Get Organization Limits

Retrieves organization limits from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-organization-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-organization-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-organization-limits?${params}`, {
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
      "emailAndTemplate": {},
      "export": {},
      "timer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAndTemplate` | object | Email and template quota information. |
| `export` | object | Export quota information. |
| `timer` | object | Timer quota information. |

## Native endpoint

Through the native Stripo API, this operation is `GET /organizationLimits` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-limits.md) for the provider-specific parameters and requirements.

