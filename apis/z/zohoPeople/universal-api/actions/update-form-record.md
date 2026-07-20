# Zoho People: Update Form Record

Updates a record in a Zoho People form.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-form-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-form-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formLinkName": "https://example.com",
  "recordId": "string",
  "inputData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-form-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formLinkName": "https://example.com",
    "recordId": "string",
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
| `recordId` | string | yes | Record ID of the Zoho People record to update. |
| `inputData` | string | yes | Zoho form field payload containing the fields to update. |
| `isDraft` | boolean | no | Set to true to save the updated record as a draft. |
| `tabularData` | string | no | Optional tabular section payload for rows that should be added, updated, or deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho People API returns.

## Native endpoint

Through the native Zoho People API, this operation is `POST /api/forms/json/:formLinkName/updateRecord` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-record.md) for the provider-specific parameters and requirements.

