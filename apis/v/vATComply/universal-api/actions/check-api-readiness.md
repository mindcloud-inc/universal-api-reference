# VAT Comply: Check API Readiness

Retrieves API readiness status from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-readiness
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-readiness?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-readiness?${params}`, {
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
      "checks": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checks` | object |  |
| `status` | string |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /ready` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-api-readiness.md) for the provider-specific parameters and requirements.

