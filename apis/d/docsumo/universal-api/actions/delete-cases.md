# Docsumo: Delete Cases

Deletes existing cases from a Docsumo case type.

```
DELETE https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-cases?connectionId=$CONNECTION_ID&case_ids%5B%5D=string&casetype_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "case_ids[]": "string",
  "casetype_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-cases?${params}`, {
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
| `case_ids[]` | array<string> | yes | One or more case IDs to delete. |
| `casetype_id` | string | yes | Docsumo case type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | string |  |
| `error_code` | string |  |
| `message` | string |  |
| `source` | string |  |
| `status` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native Docsumo API, this operation is `POST /api/v1/external/agents/:casetype_id/cases/bulk/delete` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-cases.md) for the provider-specific parameters and requirements.

