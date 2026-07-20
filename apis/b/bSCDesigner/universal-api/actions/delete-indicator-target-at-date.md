# BSC Designer: Delete Indicator Target At Date



```
DELETE https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-target-at-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-target-at-date?connectionId=$CONNECTION_ID&documentId=string&indicatorGuid=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "indicatorGuid": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-target-at-date?${params}`, {
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
| `documentId` | string | yes | Document id |
| `indicatorGuid` | string | yes | Indicator guid |
| `date` | string | yes | Date (yyyy-MM-dd) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BSC Designer API returns.

## Native endpoint

Through the native BSC Designer API, this operation is `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/target/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-indicator-target-at-date.md) for the provider-specific parameters and requirements.

