# Docmosis: List Templates



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-templates?${params}`, {
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
| `folder` | string | no | Optional folder path to start listing from. Example: `/mindcloud/stage3`. |
| `includeSubFolders` | boolean | no | Whether to include templates inside subfolders. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeDetail` | boolean | no | Include template metadata in the listing. Example: `false`. |
| `paging` | boolean | no | Whether to return paged results. Example: `false`. |
| `pageToken` | string | no | Token for the next results page when paging is enabled. Example: `next-page-token`. |
| `pageSize` | number | no | Page size when paging is enabled. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
      "nextPageToken": "string",
      "pageSize": "string",
      "shortMsg": "string",
      "succeeded": true,
      "templateList": [
        {
          "isSystemTemplate": "string",
          "lastModifiedISO8601": "string",
          "lastModifiedMillisSinceEpoch": "string",
          "md5": "string",
          "name": "Ava Chen",
          "sizeBytes": "string",
          "templateDescription": "string",
          "templateDevMode": "string",
          "templateHasErrors": "string",
          "templatePlainTextFieldPrefix": "string",
          "templatePlainTextFieldSuffix": "string"
        }
      ],
      "templateListStale": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `longMsg` | string |  |
| `nextPageToken` | string |  |
| `pageSize` | string |  |
| `shortMsg` | string |  |
| `succeeded` | boolean |  |
| `templateList` | array<object> |  |
| `templateList[].isSystemTemplate` | string |  |
| `templateList[].lastModifiedISO8601` | string |  |
| `templateList[].lastModifiedMillisSinceEpoch` | string |  |
| `templateList[].md5` | string |  |
| `templateList[].name` | string |  |
| `templateList[].sizeBytes` | string |  |
| `templateList[].templateDescription` | string |  |
| `templateList[].templateDevMode` | string |  |
| `templateList[].templateHasErrors` | string |  |
| `templateList[].templatePlainTextFieldPrefix` | string |  |
| `templateList[].templatePlainTextFieldSuffix` | string |  |
| `templateListStale` | string |  |

## Native endpoint

Through the native Docmosis API, this operation is `POST /listTemplates` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

