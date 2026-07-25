# Sage Intacct: Create So Transaction



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-so-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-so-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactiontype": "string",
  "fields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-so-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactiontype": "string",
    "fields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newfields[].fieldName` | string | no |  |
| `newfields[].internalFields[].fieldValue` | string | no |  |
| `transactiontype` | string | yes |  |
| `fields` | string<object> | yes |  |
| `newfields[].fieldValue` | string | no |  |
| `newfields[].internalFields[].fieldName` | string | no |  |
| `entityID` | string | no |  |
| `newfields[].fieldIterator` | string | no |  |
| `newfields[].internalFields[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "controlid": "string",
      "function": "string",
      "key": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `controlid` | string |  |
| `function` | string |  |
| `key` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sage Intacct API, this operation is `POST https://api.intacct.com/ia/xml/xmlgw.phtml` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-so-transaction.md) for the provider-specific parameters and requirements.

