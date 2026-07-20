# Bigin by Zoho CRM: List Related Records

Retrieves related records for a Bigin by Zoho CRM record.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-related-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-related-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Accounts&recordId=string&relatedListApiName=Contacts&fields=Full_Name%2CEmail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Accounts",
  "recordId": "string",
  "relatedListApiName": "Contacts",
  "fields": "Full_Name,Email"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-related-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | list<string> | yes | Supported parent module API name. Official docs limit this endpoint to Contacts, Pipelines, Accounts, and Products. One of: `Accounts`, `Contacts`, `Pipelines`, `Products`. |
| `recordId` | string | yes | The ID of the parent record whose related records you want to fetch. |
| `relatedListApiName` | string | yes | The API name of the related list to fetch for the parent record. Example: `Contacts`. |
| `fields` | string | yes | Comma-separated field API names to include from the related-list records. Example: `Full_Name,Email`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `GET /:module_api_name/:record_id/:related_list_api_name` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-related-records.md) for the provider-specific parameters and requirements.

