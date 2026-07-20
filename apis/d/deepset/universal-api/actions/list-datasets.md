# Deepset: List Datasets

Retrieves datasets from a Deepset workspace.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/list-datasets?${params}`, {
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
| `workspaceName` | string | yes | deepset workspace name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "file_names": [
            "Ava Chen"
          ],
          "name": "Ava Chen"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].file_names[]` | string |  |
| `data[].name` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/workspaces/:workspace_name/datasets` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

