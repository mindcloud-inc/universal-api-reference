# Seqera: List Datasets

Retrieves datasets from a Seqera workspace.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-datasets?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-datasets?${params}`, {
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
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasets": [
        {
          "dateCreated": "2026-05-07T12:00:00.000Z",
          "deleted": true,
          "description": "string",
          "hidden": true,
          "id": "string",
          "lastUpdated": "2026-05-07T12:00:00.000Z",
          "mediaType": "string",
          "name": "Ava Chen",
          "organizationId": 1,
          "runsInfo": {
            "lastUsed": "2026-05-07T12:00:00.000Z",
            "runsCount": 1
          },
          "sourceType": "string",
          "version": 1,
          "workspaceId": 1
        }
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasets` | array<object> | Workspace datasets. |
| `datasets[].dateCreated` | date | Dataset creation timestamp. |
| `datasets[].deleted` | boolean | Whether the dataset is deleted. |
| `datasets[].description` | string | Dataset description. |
| `datasets[].hidden` | boolean | Whether the dataset is hidden. |
| `datasets[].id` | string | Dataset ID. |
| `datasets[].lastUpdated` | date | Dataset update timestamp. |
| `datasets[].mediaType` | string | Dataset media type. |
| `datasets[].name` | string | Dataset name. |
| `datasets[].organizationId` | number | Organization ID. |
| `datasets[].runsInfo` | object | Run usage metadata. |
| `datasets[].runsInfo.lastUsed` | date | Last run usage timestamp. |
| `datasets[].runsInfo.runsCount` | number | Number of runs using the dataset. |
| `datasets[].sourceType` | string | Dataset source type. |
| `datasets[].version` | number | Dataset version. |
| `datasets[].workspaceId` | number | Workspace ID. |
| `totalSize` | number | Total number of datasets returned. |

## Native endpoint

Through the native Seqera API, this operation is `GET /workspaces/:workspaceId/datasets` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

