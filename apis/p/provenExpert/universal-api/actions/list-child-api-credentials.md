# ProvenExpert: List Child API Credentials

Lists API credentials for child profiles in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-api-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-child-api-credentials?${params}`, {
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
      "id": "string",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address for the child profile. |
| `id` | string | API ID for the child profile. |
| `key` | string | API key for the child profile. |

## Native endpoint

Through the native ProvenExpert API, this operation is `GET /auth/api/children` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-api-credentials.md) for the provider-specific parameters and requirements.

