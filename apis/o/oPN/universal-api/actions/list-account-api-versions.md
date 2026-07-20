# OPN: List Account API Versions

Retrieves a list of account API versions from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-account-api-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-account-api-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-account-api-versions?${params}`, {
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
      "api_version": "string",
      "country": "string",
      "currency": "string",
      "email": "ava@example.com",
      "id": "string",
      "last_updated_api_version": "string",
      "livemode": true,
      "location": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `email` | string |  |
| `id` | string |  |
| `last_updated_api_version` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /account/api_versions` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-api-versions.md) for the provider-specific parameters and requirements.

