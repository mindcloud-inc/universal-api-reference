# PlagiarismCheck.org: Get Plagiarism Report



```
GET https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-report?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-report?${params}`, {
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
| `id` | number | yes | Plagiarism check identifier returned by Submit Plagiarism Check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "report": {
          "createdAt": "string",
          "groupId": {},
          "id": 1,
          "percent": "string",
          "sourceCount": 1,
          "textId": 1,
          "version": {}
        },
        "reportData": {
          "createdAt": "string",
          "externalQueries": 1,
          "indexes": [
            {
              "dbId": 1,
              "id": 1,
              "name": "Ava Chen",
              "queries": 1,
              "status": "string",
              "type": "string"
            }
          ],
          "length": 1,
          "matchedLength": 1,
          "matchedPercent": 1,
          "nodes": [
            {
              "enabled": true,
              "end": 1,
              "start": 1,
              "text": "string"
            }
          ],
          "sourcesCount": 1,
          "version": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.report.createdAt` | string |  |
| `data.report.groupId` | object |  |
| `data.report.id` | number |  |
| `data.report.percent` | string |  |
| `data.report.sourceCount` | number |  |
| `data.report.textId` | number |  |
| `data.report.version` | object |  |
| `data.reportData.createdAt` | string |  |
| `data.reportData.externalQueries` | number |  |
| `data.reportData.indexes[].dbId` | number |  |
| `data.reportData.indexes[].id` | number |  |
| `data.reportData.indexes[].name` | string |  |
| `data.reportData.indexes[].queries` | number |  |
| `data.reportData.indexes[].status` | string |  |
| `data.reportData.indexes[].type` | string |  |
| `data.reportData.length` | number |  |
| `data.reportData.matchedLength` | number |  |
| `data.reportData.matchedPercent` | number |  |
| `data.reportData.nodes[].enabled` | boolean |  |
| `data.reportData.nodes[].end` | number |  |
| `data.reportData.nodes[].start` | number |  |
| `data.reportData.nodes[].text` | string |  |
| `data.reportData.sourcesCount` | number |  |
| `data.reportData.version` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `GET /api/v1/text/report/:id` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plagiarism-report.md) for the provider-specific parameters and requirements.

