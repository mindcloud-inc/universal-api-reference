# Sage Intacct: Create Journal



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createjournal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createjournal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "journal": "string",
  "batchDate": "string",
  "batchTitle": "string",
  "entries[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createjournal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "journal": "string",
    "batchDate": "string",
    "batchTitle": "string",
    "entries[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entries[].department` | string | no |  |
| `journal` | string | yes |  |
| `batchDate` | string | yes |  |
| `entries[].glaccount` | string | no |  |
| `batchTitle` | string | yes |  |
| `entries[].trType` | string | no |  |
| `entries[]` | array | yes |  |
| `entries[].amount` | number | no |  |
| `entries[].classID` | string | no |  |
| `entries[].location` | string | no |  |
| `entries[].itemID` | string | no |  |
| `entries[].description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/createjournal.md) for the provider-specific parameters and requirements.

