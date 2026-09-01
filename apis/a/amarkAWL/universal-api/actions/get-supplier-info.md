# Amark: Get Supplier Info



```
GET https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-supplier-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-supplier-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-supplier-info?${params}`, {
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
      "context": "string",
      "event": "string",
      "status": 1,
      "successData": {
        "contactEmail": "ava@example.com",
        "contactName": "Ava Chen",
        "contactPhone": "string",
        "id": 1,
        "name": "Ava Chen",
        "supplierModifyId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `event` | string |  |
| `status` | number |  |
| `successData.contactEmail` | string |  |
| `successData.contactName` | string |  |
| `successData.contactPhone` | string |  |
| `successData.id` | number |  |
| `successData.name` | string |  |
| `successData.supplierModifyId` | number |  |

## Native endpoint

Through the native Amark API, this operation is `POST /Supplier/Info` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier-info.md) for the provider-specific parameters and requirements.

