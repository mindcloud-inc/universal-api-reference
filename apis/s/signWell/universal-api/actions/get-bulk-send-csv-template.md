# SignWell: Get Bulk Send CSV Template

Retrieves a bulk send CSV template from SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-csv-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-csv-template?connectionId=$CONNECTION_ID&templateIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-csv-template?${params}`, {
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
| `templateIds[]` | array<string> | yes | One or more template IDs to generate a blank CSV template. |
| `base64` | boolean | no | When true, returns the CSV as a base64-encoded string in a JSON response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignWell API returns.

## Native endpoint

Through the native SignWell API, this operation is `GET /bulk_sends/csv_template` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-send-csv-template.md) for the provider-specific parameters and requirements.

