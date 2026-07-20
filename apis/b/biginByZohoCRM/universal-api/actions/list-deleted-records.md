# Bigin by Zoho CRM: List Deleted Records

Retrieves deleted records from a Bigin by Zoho CRM module.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-deleted-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-deleted-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Accounts"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-deleted-records?${params}`, {
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
| `moduleApiName` | list<string> | yes | Supported module API name for deleted-record retrieval. One of: `Accounts`, `Calls`, `Contacts`, `Events`, `Pipelines`, `Products`, `Tasks`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list<string> | no | Which deleted-record bucket to return. One of: `all`, `permanent`, `recycle`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `GET /:module_api_name/deleted` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deleted-records.md) for the provider-specific parameters and requirements.

