# Documentum: List Workflow Tasks



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-workflow-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-workflow-tasks?connectionId=$CONNECTION_ID&repositoryName=d2repo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-workflow-tasks?${params}`, {
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
| `inline` | boolean | no | When true, include elaborated task details in the response. Default: `true`. |

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
| `entries[].id` | string | Task entry identifier. |
| `entries[].links[].href` | string | Task link URL. |
| `entries[].links[].rel` | string | Task link relation. |
| `entries[].status` | string | Task status. |
| `entries[].title` | string | Task title. |
| `id` | string | Task list feed identifier. |
| `title` | string | Task list title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/tasklist` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-tasks.md) for the provider-specific parameters and requirements.

