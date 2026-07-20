# Bigin by Zoho CRM: List Record Attachments

Retrieves attachments for a record in Bigin by Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-record-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-record-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Ava%20Chen&recordId=7319088000000000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Ava Chen",
  "recordId": "7319088000000000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-record-attachments?${params}`, {
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
| `moduleApiName` | list<string> | yes | The API name of the parent module. |
| `recordId` | string | yes | The ID of the parent record. Example: `7319088000000000001`. |
| `fields` | string | no | Comma-separated attachment fields to return. Example: `File_Name,Size`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `GET /:moduleApiName/:recordId/Attachments` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-record-attachments.md) for the provider-specific parameters and requirements.

