# Reportei: Get Report

Retrieves a report from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-report?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-report?${params}`, {
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
| `id` | number | yes | ID do relatório. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report": {
        "external_url": "https://example.com",
        "id": 1,
        "internal_url": "https://example.com",
        "subtitle": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report.external_url` | string | Public report URL |
| `report.id` | number | Report identifier |
| `report.internal_url` | string | Internal report URL |
| `report.subtitle` | string | Report subtitle |
| `report.title` | string | Report title |

## Native endpoint

Through the native Reportei API, this operation is `GET /reports/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

