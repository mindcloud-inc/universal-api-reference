# Peggy Pay: Add Submission Item

Updates a Peggy Pay submission by adding an item.

```
PUT https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/add-submission-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peggy Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/add-submission-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hash": "abc123submissionhash",
  "itemKey": "externalReference",
  "itemLabel": "External reference",
  "itemValue": "ORD-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/add-submission-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hash": "abc123submissionhash",
    "itemKey": "externalReference",
    "itemLabel": "External reference",
    "itemValue": "ORD-1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hash` | string | yes | Submission hash to update. Example: `abc123submissionhash`. |
| `itemKey` | string | yes | Unique item key; existing keys are overwritten by Peggy Pay. Example: `externalReference`. |
| `itemLabel` | string | yes | Human-readable item label. Example: `External reference`. |
| `itemValue` | string | yes | Item value to store on the submission. Example: `ORD-1001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Additional Peggy Pay response data when present. |
| `message` | string | Peggy Pay response message when present. |
| `success` | boolean | Whether Peggy Pay accepted the addItem request. |

## Native endpoint

Through the native Peggy Pay API, this operation is `GET Formbuilder.Submissions.addItem` (base URL `https://www.peggypay.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-submission-item.md) for the provider-specific parameters and requirements.

