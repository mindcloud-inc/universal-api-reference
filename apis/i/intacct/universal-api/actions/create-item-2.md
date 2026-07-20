# Sage Intacct: Create Item New



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-item-2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-item-2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "PROJECT",
  "fields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-item-2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "PROJECT",
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
| `object` | string | yes | Default: `PROJECT`. |
| `fields` | string<object> | yes |  |
| `newfields[].fieldValue` | string | no |  |
| `newfields[].internalFields[].fieldName` | string | no |  |
| `entityID` | string | no |  |
| `newfields[].fieldIterator` | string | no |  |
| `newfields[].internalFields[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item-2.md) for the provider-specific parameters and requirements.

