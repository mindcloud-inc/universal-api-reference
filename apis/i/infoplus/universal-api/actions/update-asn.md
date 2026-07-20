# Infoplus: Update ASN

Updates an existing ASN in Infoplus.

```
PUT https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-asn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-asn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-asn', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "poNo": "string",
      "status": "string",
      "vendorId": 1,
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `id` | number |  |
| `modifyDate` | date |  |
| `poNo` | string |  |
| `status` | string |  |
| `vendorId` | number |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Infoplus API, this operation is `PUT /asn` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asn.md) for the provider-specific parameters and requirements.

