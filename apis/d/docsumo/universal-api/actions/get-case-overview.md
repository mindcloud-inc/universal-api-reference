# Docsumo: Get Case Overview

Retrieves overview details for a Docsumo case.

```
GET https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-case-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-case-overview?connectionId=$CONNECTION_ID&case_id=string&casetype_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "case_id": "string",
  "casetype_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/get-case-overview?${params}`, {
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
| `case_id` | string | yes | Docsumo case ID. |
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

Through the native Docsumo API, this operation is `GET /api/v1/external/agents/:casetype_id/case/:case_id` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-overview.md) for the provider-specific parameters and requirements.

