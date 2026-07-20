# Documentum: Export Object Audit



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/export-object-audit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/export-object-audit?connectionId=$CONNECTION_ID&repositoryName=d2repo&objectId=090000018000abcd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "objectId": "090000018000abcd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/export-object-audit?${params}`, {
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
| `objectId` | string | yes | Documentum object or workflow ID whose audit should be exported. Example: `090000018000abcd`. |
| `allVersions` | boolean | no | When true, export audit data for all versions. Defaults to true. Default: `true`. |
| `exportType` | string | no | Audit export file type. The documented value is XLSX. Default: `XLSX`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Optional audit filter expression. Example: `contains(event_name,'approve')`. |
| `fileName` | string | no | Optional custom audit export file name. Example: `audit-export.xlsx`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentLength": 1,
      "contentType": "string",
      "exportType": "string",
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentLength` | number | Returned file content length. |
| `contentType` | string | Returned file content type. |
| `exportType` | string | Audit export format. |
| `fileName` | string | Audit export file name. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/objects/{objectId}/audit-export` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-object-audit.md) for the provider-specific parameters and requirements.

