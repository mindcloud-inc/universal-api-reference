# Rownd Data Privacy: Get Sample User Profile Data



```
GET https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data?${params}`, {
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
      "data": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Sample user profile payload. |
| `state` | string | Sample user state. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `GET /users/__sample__/data` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-user-profile-data.md) for the provider-specific parameters and requirements.

