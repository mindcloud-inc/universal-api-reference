# Maildroppa: Update Subscriber Field



```
PUT https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-subscriber-field', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataType` | string | no | Data type of the field. |
| `id` | string | no | Unique identifier of the field type. |
| `name` | string | no | Display name of the field type. |
| `optionValues[]` | array | no | List of allowable option values if the data type supports choices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataType": "string",
      "id": "string",
      "name": "Ava Chen",
      "optionValues": [
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
| `dataType` | string | Data type of the field. |
| `id` | string | Unique identifier of the field type. |
| `name` | string | Display name of the field type. |
| `optionValues` | array<string> | List of allowable option values if the data type supports choices. |

## Native endpoint

Through the native Maildroppa API, this operation is `PUT /field-type` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber-field.md) for the provider-specific parameters and requirements.

