# Lasso X: Get Latest Report

Retrieves the latest report for a CVR entity from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-latest-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-latest-report?connectionId=$CONNECTION_ID&lasso_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lasso_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-latest-report?${params}`, {
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
| `lasso_id` | string | yes | Lasso ID, for example CVR-1-34580820. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": {
        "unit": "string",
        "value": 1
      },
      "currencies": [
        "string"
      ],
      "cvr": 1,
      "documents": [
        {
          "mimeType": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "equity": {
        "value": 1
      },
      "period": {
        "from": "2026-05-07T12:00:00.000Z",
        "to": "2026-05-07T12:00:00.000Z"
      },
      "publicationTime": "2026-05-07T12:00:00.000Z",
      "reportType": "string",
      "reportUrl": "https://example.com",
      "reportYear": 1,
      "result": {
        "value": 1
      },
      "revenue": {
        "value": 1
      },
      "xbrlUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets.unit` | string |  |
| `assets.value` | number |  |
| `currencies[]` | string |  |
| `cvr` | number |  |
| `documents[].mimeType` | string |  |
| `documents[].type` | string |  |
| `documents[].url` | string |  |
| `equity.value` | number |  |
| `period.from` | date |  |
| `period.to` | date |  |
| `publicationTime` | date |  |
| `reportType` | string |  |
| `reportUrl` | string |  |
| `reportYear` | number |  |
| `result.value` | number |  |
| `revenue.value` | number |  |
| `xbrlUrl` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /:lassoId/reports/latest` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-report.md) for the provider-specific parameters and requirements.

