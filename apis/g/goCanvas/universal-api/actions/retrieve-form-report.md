# GoCanvas: Retrieve Form Report



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form-report?connectionId=$CONNECTION_ID&formId=1&reportId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1",
  "reportId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form-report?${params}`, {
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
| `formId` | number | yes |  |
| `reportId` | number | yes | Use -2 for a Quick Start or Designer PDF when returned by List Form Reports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultEmailed": true,
      "definition": "string",
      "format": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `defaultEmailed` | boolean |  |
| `definition` | string |  |
| `format` | string |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /forms/:formId/reports/:reportId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form-report.md) for the provider-specific parameters and requirements.

