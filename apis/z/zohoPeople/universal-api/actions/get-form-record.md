# Zoho People: Get Form Record

Retrieves a record from a Zoho People form.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-record?connectionId=$CONNECTION_ID&formLinkName=https%3A%2F%2Fexample.com&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formLinkName": "https://example.com",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-record?${params}`, {
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
| `recordId` | string | yes | Record ID from Zoho People, typically obtained from a bulk-records or search response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho People API returns.

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms/:formLinkName/getDataByID` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-record.md) for the provider-specific parameters and requirements.

