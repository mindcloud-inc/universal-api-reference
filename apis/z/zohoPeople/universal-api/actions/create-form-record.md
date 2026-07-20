# Zoho People: Create Form Record

Creates a record in a Zoho People form.

```
POST https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/create-form-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/create-form-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formLinkName": "https://example.com",
  "inputData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/create-form-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formLinkName": "https://example.com",
    "inputData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formLinkName` | string | yes | Zoho People formLinkName. Example: employee. |
| `inputData` | string | yes | Zoho form field payload, for example {Single_Line_1:"a1",Lookup_1:"705358000000229001"}. |
| `isDraft` | boolean | no | Set to true to save the record as a draft. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho People API returns.

## Native endpoint

Through the native Zoho People API, this operation is `POST /api/forms/json/:formLinkName/insertRecord` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-record.md) for the provider-specific parameters and requirements.

