# VAT Comply: Get API Information

Retrieves API information from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-api-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-api-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/get-api-information?${params}`, {
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
      "contact": "string",
      "description": "string",
      "documentation": "string",
      "endpoints": {},
      "name": "Ava Chen",
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
| `contact` | string |  |
| `description` | string |  |
| `documentation` | string |  |
| `endpoints` | object |  |
| `name` | string |  |
| `status` | string |  |
| `version` | string |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-information.md) for the provider-specific parameters and requirements.

