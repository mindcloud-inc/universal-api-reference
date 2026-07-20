# Marketing Master IO: Get Custom Variable

Retrieves a custom variable from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-custom-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-custom-variable?connectionId=$CONNECTION_ID&variable_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variable_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-custom-variable?${params}`, {
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
| `variable_key` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_created": "2026-05-07T12:00:00.000Z",
      "google_sheet_data": {
        "column": "string",
        "sheet": "string",
        "sheet_id": "string"
      },
      "id": "string",
      "is_native": "string",
      "name": "Ava Chen",
      "user_id": "string",
      "variable_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `google_sheet_data.column` | string |  |
| `google_sheet_data.sheet` | string |  |
| `google_sheet_data.sheet_id` | string |  |
| `id` | string |  |
| `is_native` | string |  |
| `name` | string |  |
| `user_id` | string |  |
| `variable_key` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/messenger/custom_variables/:variable_key` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-variable.md) for the provider-specific parameters and requirements.

