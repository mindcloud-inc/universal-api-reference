# Bigin by Zoho CRM: Update Related Records

Updates related records for a Bigin by Zoho CRM record.

```
PUT https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/update-related-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/update-related-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "relatedListApiName": "Ava Chen",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/update-related-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string",
    "relatedListApiName": "Ava Chen",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | string | yes | The parent Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `recordId` | string | yes | The parent Bigin record identifier. |
| `relatedListApiName` | string | yes | The Bigin related-list API name to update under the parent record. |
| `data[]` | array<object> | yes | Array of related-record objects to update. Each object should include the related record id and the fields to change. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `PUT /:module_api_name/:record_id/:related_list_api_name` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-related-records.md) for the provider-specific parameters and requirements.

