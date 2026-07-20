# Alpha TransForm: List Users In Account

Retrieves account users from Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-users-in-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-users-in-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-users-in-account?${params}`, {
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
      "dateCreated": "string",
      "displayname": "Ava Chen",
      "invitedBy": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `displayname` | string |  |
| `invitedBy` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /getUsersInTransformAccount` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users-in-account.md) for the provider-specific parameters and requirements.

