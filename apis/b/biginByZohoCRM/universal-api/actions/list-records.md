# Bigin by Zoho CRM: List Records

Retrieves records from a Bigin by Zoho CRM module.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Ava%20Chen&fields=Last_Name%2CEmail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Ava Chen",
  "fields": "Last_Name,Email"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/list-records?${params}`, {
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
| `moduleApiName` | list<string> | yes | The API name of the module whose records you want to fetch. |
| `fields` | string | yes | Comma-separated field API names to include in the response. Example: `Last_Name,Email`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Field API name to sort the returned records by. Example: `Modified_Time`. |
| `sortOrder` | list<string> | no | Sort direction for the requested records. One of: `asc`, `desc`. |
| `approved` | list<string> | no | Choose whether to fetch only approved, only unapproved, or both record sets. One of: `approved`, `both`, `unapproved`. |
| `cvid` | string | no | Custom view ID to restrict the returned records. |
| `pageToken` | string | no | Token used to continue pagination from a previous response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `GET /:module_api_name` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

