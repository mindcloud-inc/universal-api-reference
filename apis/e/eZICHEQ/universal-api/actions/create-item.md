# EZICHEQ: Create Item

Creates an item in EZICHEQ.

```
POST https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZICHEQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item.itemTypeId": "string",
  "item.labelNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item.itemTypeId": "string",
    "item.labelNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item.assetDescription` | string | no |  |
| `item.itemTypeId` | string | yes |  |
| `item.itemTypeId` | string | no |  |
| `item.labelNumber` | string | no |  |
| `item.serialNumber` | string | no |  |
| `item.labelNumber` | string | yes |  |
| `item.serialNumber` | string | no |  |
| `item.assetDescription` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "date": "string",
      "error": "string",
      "request_method": "string",
      "request_uri": "string",
      "results": {},
      "status": "string",
      "status_code": 1,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `date` | string |  |
| `error` | string |  |
| `request_method` | string |  |
| `request_uri` | string |  |
| `results` | object |  |
| `status` | string |  |
| `status_code` | number |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native EZICHEQ API, this operation is `POST /item/v1` (base URL `https://api.ezicheq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

