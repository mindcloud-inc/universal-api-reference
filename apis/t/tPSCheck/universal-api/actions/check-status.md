# TPSCheck: Check status



```
GET https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TPSCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-status?${params}`, {
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
      "status": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API health status. |
| `version` | string | Current API version identifier. |

## Native endpoint

Through the native TPSCheck API, this operation is `GET /status` (base URL `https://api.tpscheck.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-status.md) for the provider-specific parameters and requirements.

