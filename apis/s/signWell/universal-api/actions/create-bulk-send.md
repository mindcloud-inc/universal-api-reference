# SignWell: Create Bulk Send

Creates a new bulk send in SignWell.

```
POST https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-bulk-send
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-bulk-send" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateIds[]": [
    "string"
  ],
  "bulkSendCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-bulk-send', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateIds[]": ["string"],
    "bulkSendCsv": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateIds[]` | array<string> | yes | Unique identifiers for a list of templates. |
| `bulkSendCsv` | string | yes | A RFC 4648 base64 string of the template CSV file to be validated. |
| `skipRowErrors` | boolean | no | Whether to skip errors in the rows. Defaults to false. |
| `apiApplicationId` | string | no | Unique identifier for API Application settings to use. |
| `name` | string | no | The name of the Bulk Send. |
| `subject` | string | no | Email subject for the signature request that recipients will see. |
| `message` | string | no | Email message for the signature request that recipients will see. |
| `applySigningOrder` | boolean | no | When true recipients will sign one at a time in the documented order. |
| `customRequesterName` | string | no | Sets the custom requester name for the document. |
| `customRequesterEmail` | string | no | Sets the custom requester email for the document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignWell API returns.

## Native endpoint

Through the native SignWell API, this operation is `POST /bulk_sends` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-send.md) for the provider-specific parameters and requirements.

