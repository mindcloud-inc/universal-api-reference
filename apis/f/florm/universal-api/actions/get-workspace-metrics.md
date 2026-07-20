# Florm: Get Workspace Metrics

Retrieves metrics for a Florm workspace.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-workspace-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-workspace-metrics?connectionId=$CONNECTION_ID&workspaceGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-workspace-metrics?${params}`, {
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
| `workspaceGuid` | string | yes | GUID of the Florm workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answersCount": 1,
      "guid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answersCount` | number | Number of answers recorded for the form. |
| `guid` | string | GUID of the Florm form. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/workspaces/:workspace_guid/metrics` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-metrics.md) for the provider-specific parameters and requirements.

