# Galileo: Query Dataset Versions

Finds versions for a Galileo dataset by query.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-dataset-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-dataset-versions?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-dataset-versions?${params}`, {
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
| `datasetId` | string | yes | Galileo dataset UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1,
      "versions": [
        {
          "columnNames": [
            "Ava Chen"
          ],
          "columnsAdded": 1,
          "columnsRemoved": 1,
          "columnsRenamed": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdByUser": {},
          "name": "Ava Chen",
          "numRows": 1,
          "rowsAdded": 1,
          "rowsEdited": 1,
          "rowsRemoved": 1,
          "versionIndex": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |
| `versions` | array<object> |  |
| `versions[].columnNames` | array<string> |  |
| `versions[].columnsAdded` | number |  |
| `versions[].columnsRemoved` | number |  |
| `versions[].columnsRenamed` | number |  |
| `versions[].createdAt` | date |  |
| `versions[].createdByUser` | object |  |
| `versions[].name` | string |  |
| `versions[].numRows` | number |  |
| `versions[].rowsAdded` | number |  |
| `versions[].rowsEdited` | number |  |
| `versions[].rowsRemoved` | number |  |
| `versions[].versionIndex` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/datasets/:dataset_id/versions/query` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-dataset-versions.md) for the provider-specific parameters and requirements.

