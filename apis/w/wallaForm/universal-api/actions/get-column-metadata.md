# Walla Form: Get Column Metadata



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-column-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-column-metadata?connectionId=$CONNECTION_ID&workspaceKey=string&projectKey=string&columnKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceKey": "string",
  "projectKey": "string",
  "columnKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-column-metadata?${params}`, {
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
| `workspaceKey` | string | yes | The Walla workspace key. |
| `projectKey` | string | yes | The Walla project key. |
| `columnKey` | string | yes | The column key for a project field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "column_name": "Ava Chen",
      "label": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `column_name` | string |  |
| `label` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Walla Form API, this operation is `GET /workspace/:workspaceKey/project/:projectKey/response/list/:columnKey` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column-metadata.md) for the provider-specific parameters and requirements.

