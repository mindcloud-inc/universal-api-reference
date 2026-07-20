# Spondyr: Update Condition

Updates an existing condition for a transaction type in Spondyr.

```
PUT https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/update-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/update-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionType": "string",
  "condition": "string",
  "name": "Ava Chen",
  "fieldName": "Ava Chen",
  "possibleValues": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/update-condition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionType": "string",
    "condition": "string",
    "name": "Ava Chen",
    "fieldName": "Ava Chen",
    "possibleValues": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionType` | string | yes | The transaction type the condition belongs to. |
| `condition` | string | yes | The existing condition name to update. |
| `name` | string | yes | The new condition name. |
| `fieldName` | string | yes | The field name the condition evaluates. |
| `possibleValues` | string | yes | The newline-delimited possible values for the condition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "APIStatus": "string",
      "ErrorMessage": "string",
      "ReferenceID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIStatus` | string |  |
| `ErrorMessage` | string |  |
| `ReferenceID` | string | Updated condition identifier. |

## Native endpoint

Through the native Spondyr API, this operation is `PUT /Condition` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-condition.md) for the provider-specific parameters and requirements.

