# Templated: Get Account Information

Retrieves detailed account information from Templated.

```
GET https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information?${params}`, {
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
      "apiQuota": 1,
      "apiUsage": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "plan": "string",
      "teamName": "Ava Chen",
      "usagePercentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiQuota` | number |  |
| `apiUsage` | number |  |
| `email` | string |  |
| `name` | string |  |
| `plan` | string |  |
| `teamName` | string |  |
| `usagePercentage` | number |  |

## Native endpoint

Through the native Templated API, this operation is `GET /v1/account` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

