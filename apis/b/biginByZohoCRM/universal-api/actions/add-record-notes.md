# Bigin by Zoho CRM: Add Record Notes

Creates notes for a record in Bigin by Zoho CRM.

```
POST https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/add-record-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/add-record-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/add-record-notes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | string | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `recordId` | string | yes | The Bigin record identifier that should receive the note. |
| `data[]` | array<object> | yes | Array of note objects to create for the target record. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `POST /:module_api_name/:record_id/Notes` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-record-notes.md) for the provider-specific parameters and requirements.

