# Documentum: Get Workflow Report Tasks



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-report-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-report-tasks?connectionId=$CONNECTION_ID&repositoryName=d2repo&workflowId=4d00000180001234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "workflowId": "4d00000180001234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-workflow-report-tasks?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `workflowId` | string | yes | Workflow ID whose report tasks should be returned. Example: `4d00000180001234`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterName` | string | no | Optional D2-Config workflow filter name. Example: `Open Tasks`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {
          "id": "string",
          "links": [
            {
              "href": "https://example.com",
              "rel": "https://example.com"
            }
          ],
          "status": "string",
          "title": "string"
        }
      ],
      "id": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries[].id` | string | Report task identifier. |
| `entries[].links[].href` | string | Report task link URL. |
| `entries[].links[].rel` | string | Report task link relation. |
| `entries[].status` | string | Report task status. |
| `entries[].title` | string | Report task title. |
| `id` | string | Workflow report feed identifier. |
| `title` | string | Workflow report title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/d2-workflows/{workflowId}/d2-report-tasks` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-report-tasks.md) for the provider-specific parameters and requirements.

