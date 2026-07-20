# Oneflow: Update Contract Data Field Value

Updates a contract data field value in Oneflow.

```
PUT https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contract-data-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contract-data-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string",
  "dataFieldId": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contract-data-field-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string",
    "dataFieldId": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractId` | string | yes | The Oneflow contract ID. |
| `dataFieldId` | string | yes | The Oneflow contract data field ID. |
| `value` | string | yes | The desired value for the data field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "custom_id": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "placeholder": "string",
      "source": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `custom_id` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `placeholder` | string |  |
| `source` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `PUT /contracts/:contractId/data_fields/:dataFieldId` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contract-data-field-value.md) for the provider-specific parameters and requirements.

