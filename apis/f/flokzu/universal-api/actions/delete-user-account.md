# Flokzu: Delete User Account



```
DELETE https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/delete-user-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/delete-user-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/delete-user-account?${params}`, {
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
      "detail": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Flokzu API, this operation is `DELETE /v1/management/user` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-account.md) for the provider-specific parameters and requirements.

