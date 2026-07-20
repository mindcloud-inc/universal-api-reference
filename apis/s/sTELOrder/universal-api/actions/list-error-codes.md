# STEL Order: List Error Codes

Retrieves a list of STEL Order API error codes.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-error-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-error-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-error-codes?${params}`, {
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
      "description": "string",
      "error-code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `error-code` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /errorCodes` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-error-codes.md) for the provider-specific parameters and requirements.

