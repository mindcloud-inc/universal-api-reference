# MillionVerifier: List Verification Files

Retrieves verification files from MillionVerifier.

```
GET https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/list-verification-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MillionVerifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/list-verification-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/list-verification-files?${params}`, {
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
| `offset` | number | no | Offset for pagination. Default: `0`. |
| `limit` | number | no | Maximum number of files to return. Default: `50`. |
| `id` | string | no | Comma-separated file IDs to include. Example: `1,2,3`. |
| `name` | string | no | Text that should appear in the file name. Example: `emails.csv`. |
| `status` | string | no | Comma-separated file statuses to include. Example: `finished,in_progress`. |
| `updatedAtFrom` | string | no | Only include files updated after this timestamp. Example: `2023-01-01 15:00:05`. |
| `updatedAtTo` | string | no | Only include files updated before this timestamp. Example: `2023-01-01 15:00:05`. |
| `createdateFrom` | string | no | Only include files created after this timestamp. Example: `2023-01-01 15:00:05`. |
| `createdateTo` | string | no | Only include files created before this timestamp. Example: `2023-01-01 15:00:05`. |
| `percentFrom` | number | no | Only include files with progress greater than or equal to this percentage. |
| `percentTo` | number | no | Only include files with progress less than or equal to this percentage. |
| `hasError` | string | no | Filter for files that have or do not have errors. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {
          "catchAll": 1,
          "createdate": "string",
          "credit": 1,
          "disposable": 1,
          "error": "string",
          "estimatedTimeSec": 1,
          "fileId": "string",
          "fileName": "Ava Chen",
          "invalid": 1,
          "ok": 1,
          "percent": 1,
          "reverify": 1,
          "status": "string",
          "totalRows": 1,
          "uniqueEmails": 1,
          "unknown": 1,
          "unverified": 1,
          "updatedAt": "string",
          "verified": 1
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
| `files[].catchAll` | number |  |
| `files[].createdate` | string |  |
| `files[].credit` | number |  |
| `files[].disposable` | number |  |
| `files[].error` | string |  |
| `files[].estimatedTimeSec` | number |  |
| `files[].fileId` | string |  |
| `files[].fileName` | string |  |
| `files[].invalid` | number |  |
| `files[].ok` | number |  |
| `files[].percent` | number |  |
| `files[].reverify` | number |  |
| `files[].status` | string |  |
| `files[].totalRows` | number |  |
| `files[].uniqueEmails` | number |  |
| `files[].unknown` | number |  |
| `files[].unverified` | number |  |
| `files[].updatedAt` | string |  |
| `files[].verified` | number |  |
| `total` | number |  |

## Native endpoint

Through the native MillionVerifier API, this operation is `GET https://bulkapi.millionverifier.com/bulkapi/v2/filelist` (base URL `https://api.millionverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-verification-files.md) for the provider-specific parameters and requirements.

