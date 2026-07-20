# Lemcal: Validate Authentication

Retrieves the authenticated user from Lemcal.

```
GET https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication?${params}`, {
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
      "_id": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "publicIdentifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `publicIdentifier` | string |  |

## Native endpoint

Through the native Lemcal API, this operation is `GET /me` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-authentication.md) for the provider-specific parameters and requirements.

