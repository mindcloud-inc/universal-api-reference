# Remote Retrieval: Validate User

Validates a user in Remote Retrieval.

```
GET https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remote Retrieval `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user?${params}`, {
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
      "message": "string",
      "phone": "string",
      "response_code": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address associated with the API key. |
| `message` | string | Validation result message. |
| `phone` | string | Phone number returned by the validation endpoint. |
| `response_code` | number | Remote Retrieval response code. |
| `status` | string | Validation status. |

## Native endpoint

Through the native Remote Retrieval API, this operation is `GET /api/v1/validate/user` (base URL `https://www.remoteretrieval.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-user.md) for the provider-specific parameters and requirements.

