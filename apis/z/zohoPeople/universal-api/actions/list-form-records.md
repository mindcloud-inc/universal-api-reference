# Zoho People: List Form Records

Retrieves records from a Zoho People form.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-records?connectionId=$CONNECTION_ID&formLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-records?${params}`, {
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
| `slIndex` | number | no | Record index to start fetching from. Zoho record indexes start at 1. Default: `1`. |
| `limit` | number | no | Maximum number of records to fetch in this request. Zoho documents a maximum of 200. Default: `200`. |
| `searchColumn` | string | no | Optional employee column to search, such as EMPLOYEEID or EMPLOYEEMAILALIAS. |
| `searchValue` | string | no | Value to match for the selected search column. |
| `modifiedTime` | number | no | Fetch only records added or modified after this Unix timestamp in milliseconds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho People API returns.

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms/:formLinkName/getRecords` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-records.md) for the provider-specific parameters and requirements.

