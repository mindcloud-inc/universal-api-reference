# BSC Designer: Check Document Alerts And WEB SQL Indicators



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/check-document-alerts-and-websql-indicators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/check-document-alerts-and-websql-indicators?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/check-document-alerts-and-websql-indicators?${params}`, {
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
| `docId` | string | yes | Document ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BSC Designer API returns.

## Native endpoint

Through the native BSC Designer API, this operation is `POST /rest/api/document/:docId/document-check-requests` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-document-alerts-and-websql-indicators.md) for the provider-specific parameters and requirements.

