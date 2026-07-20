# Court Drive: Delete PACER Credentials



```
DELETE https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/delete-pacer-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/delete-pacer-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/delete-pacer-credentials?${params}`, {
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
      "app_id": "string",
      "pacer_user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_id` | string |  |
| `pacer_user` | string |  |

## Native endpoint

Through the native Court Drive API, this operation is `DELETE /pacer/credentials` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pacer-credentials.md) for the provider-specific parameters and requirements.

