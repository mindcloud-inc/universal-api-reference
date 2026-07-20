# Seqera: Describe Dataset

Retrieves dataset metadata from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-dataset?connectionId=$CONNECTION_ID&datasetId=string&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-dataset?${params}`, {
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
| `attributes` | string | no |  |
| `datasetId` | string | yes |  |
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataset": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset` | object | Dataset details. |
| `dataset.dateCreated` | date | Dataset creation timestamp. |
| `dataset.deleted` | boolean | Whether the dataset is deleted. |
| `dataset.description` | string | Dataset description. |
| `dataset.hidden` | boolean | Whether the dataset is hidden. |
| `dataset.id` | string | Dataset ID. |
| `dataset.lastUpdated` | date | Dataset update timestamp. |
| `dataset.mediaType` | string | Dataset media type. |
| `dataset.name` | string | Dataset name. |
| `dataset.organizationId` | number | Organization ID. |
| `dataset.runsInfo` | object | Run usage metadata. |
| `dataset.runsInfo.lastUsed` | date | Last run usage timestamp. |
| `dataset.runsInfo.runsCount` | number | Number of runs using the dataset. |
| `dataset.sourceType` | string | Dataset source type. |
| `dataset.version` | number | Dataset version number. |
| `dataset.workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Seqera API, this operation is `GET /workspaces/:workspaceId/datasets/:datasetId/metadata` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-dataset.md) for the provider-specific parameters and requirements.

