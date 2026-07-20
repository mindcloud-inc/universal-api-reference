# Bigin by Zoho CRM: Get Record

Retrieves a record from a Bigin by Zoho CRM module.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/get-record?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/get-record?${params}`, {
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
| `moduleApiName` | list<string> | yes | The API name of the module that contains the record. |
| `recordId` | string | yes | The unique ID of the record to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `GET /:module_api_name/:record_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

