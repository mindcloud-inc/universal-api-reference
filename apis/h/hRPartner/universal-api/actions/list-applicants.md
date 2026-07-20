# HR Partner: List Applicants



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applicants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applicants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-applicants?${params}`, {
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
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstNames` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /applicants` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applicants.md) for the provider-specific parameters and requirements.

