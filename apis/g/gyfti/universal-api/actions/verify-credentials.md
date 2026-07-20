# gyfti: Verify Credentials

Verifies gyfti API credentials with an access token.

```
GET https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials?${params}`, {
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
      "state": "string",
      "user": {
        "_id": "string",
        "Company": "string",
        "Role": "string",
        "Status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | string | Logged-in state returned by gyfti. |
| `user` | object | Logged-in gyfti user object. |
| `user._id` | string |  |
| `user.Company` | string |  |
| `user.Role` | string |  |
| `user.Status` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `POST /wf/is_log` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-credentials.md) for the provider-specific parameters and requirements.

