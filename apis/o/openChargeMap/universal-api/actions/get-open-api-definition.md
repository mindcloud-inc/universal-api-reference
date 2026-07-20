# Open Charge Map: Get OpenAPI Definition



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-open-api-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-open-api-definition?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-open-api-definition?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /openapi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-open-api-definition.md) for the provider-specific parameters and requirements.

