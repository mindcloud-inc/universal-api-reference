# BSC Designer: Delete Indicator Initiative



```
DELETE https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-initiative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-initiative?connectionId=$CONNECTION_ID&docId=string&guid=string&initiativeGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "guid": "string",
  "initiativeGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/delete-indicator-initiative?${params}`, {
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
| `docId` | string | yes | Document id or alias |
| `guid` | string | yes | Indicator guid |
| `initiativeGuid` | string | yes | Initiative guid |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BSC Designer API returns.

## Native endpoint

Through the native BSC Designer API, this operation is `DELETE /rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-indicator-initiative.md) for the provider-specific parameters and requirements.

