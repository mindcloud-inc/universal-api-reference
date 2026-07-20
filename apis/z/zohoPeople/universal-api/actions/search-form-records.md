# Zoho People: Search Form Records

Finds records in a Zoho People form.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/search-form-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/search-form-records?connectionId=$CONNECTION_ID&formLinkName=https%3A%2F%2Fexample.com&searchParams=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formLinkName": "https://example.com",
  "searchParams": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/search-form-records?${params}`, {
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
| `formLinkName` | string | yes | Zoho People formLinkName. Example: employee. |
| `searchParams` | string | yes | Zoho searchParams expression, for example {searchField:'Employeestatus',searchOperator:'Is',searchText:'Active'}. |
| `slIndex` | number | no | Record index to start fetching from. Zoho record indexes start at 1. Default: `1`. |
| `limit` | number | no | Maximum number of records to fetch. Zoho documents a maximum of 200. Default: `200`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho People API returns.

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms/:formLinkName/getRecords` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-form-records.md) for the provider-specific parameters and requirements.

