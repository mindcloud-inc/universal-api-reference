# Bigin by Zoho CRM: Delete Records

Deletes existing records from a Bigin by Zoho CRM module.

```
DELETE https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/delete-records?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/delete-records?${params}`, {
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
| `moduleApiName` | string | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `ids` | string | yes | Comma-separated list of Bigin record IDs to delete. Accepts multiple values in one string, delimited by `,`. |
| `wfTrigger` | boolean | no | Whether to execute workflows for the delete request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `DELETE /:module_api_name` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

