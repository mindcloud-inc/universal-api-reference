# NetLicensing: Delete Token

Deletes an existing token from NetLicensing.

```
DELETE https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/delete-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/delete-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/delete-token?${params}`, {
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
      "number": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string |  |
| `status` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `DELETE /token/{tokenNumber}` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-token.md) for the provider-specific parameters and requirements.

