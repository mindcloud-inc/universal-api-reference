# Kite Suite: Search All Data in Workspace



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/search-all-data-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/search-all-data-in-workspace?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/search-all-data-in-workspace?${params}`, {
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
| `query` | string | yes | Search query string. |
| `selectedtype` | string | no | Type of data to filter by (task, project, epic). |
| `projects[]` | array | no | Array of project IDs to filter by. |
| `assignees[]` | array | no | Array of assignee IDs to filter by. |
| `reporters[]` | array | no | Array of reporter IDs to filter by. |
| `status` | string | no | Status to filter by (done, open). |
| `priorities[]` | array | no | Array of priorities to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        "string"
      ],
      "epics": [
        "string"
      ],
      "forms": [
        "string"
      ],
      "items": [
        "string"
      ],
      "whiteBoards": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array |  |
| `epics` | array |  |
| `forms` | array |  |
| `items` | array |  |
| `whiteBoards` | array |  |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/workspace/search/:query` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-all-data-in-workspace.md) for the provider-specific parameters and requirements.

