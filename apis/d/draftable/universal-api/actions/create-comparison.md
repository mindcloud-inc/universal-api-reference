# Draftable: Create Comparison

Creates a document comparison in Draftable.

```
POST https://connect.mindcloud.co/v1/universal/draftable/latest/actions/create-comparison
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/create-comparison" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "left.fileType": "csv",
  "right.fileType": "csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/draftable/latest/actions/create-comparison', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "left.fileType": "csv",
    "right.fileType": "csv"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `left.file` | file | no | Upload the left file, or provide Left Source URL instead. |
| `left.sourceUrl` | string | no | Source URL for the left file, or upload Left File instead. |
| `left.fileType` | string | yes | File type of the left file. One of: `csv`, `doc`, `docm`, `docx`, `odt`, `pdf`, `ppt`, `pptm`, `pptx`, `rtf`, `txt`, `xls`, `xlsm`, `xlsx`. |
| `left.displayName` | string | no | Display name for the left file. |
| `right.file` | file | no | Upload the right file, or provide Right Source URL instead. |
| `right.sourceUrl` | string | no | Source URL for the right file, or upload Right File instead. |
| `right.fileType` | string | yes | File type of the right file. One of: `csv`, `doc`, `docm`, `docx`, `odt`, `pdf`, `ppt`, `pptm`, `pptx`, `rtf`, `txt`, `xls`, `xlsm`, `xlsx`. |
| `right.displayName` | string | no | Display name for the right file. |
| `public` | boolean | no | Whether the comparison can be viewed without viewer URL signing. Default: `false`. |
| `expiryTime` | date | no | When the comparison should be automatically deleted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | no | Optional custom identifier for the comparison. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparisonType": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "identifier": "string",
      "left": {
        "fileType": "string",
        "sourceUrl": "https://example.com"
      },
      "ready": true,
      "right": {
        "fileType": "string",
        "sourceUrl": "https://example.com"
      },
      "viewerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparisonType` | string |  |
| `creationTime` | date |  |
| `identifier` | string |  |
| `left.fileType` | string |  |
| `left.sourceUrl` | string |  |
| `ready` | boolean |  |
| `right.fileType` | string |  |
| `right.sourceUrl` | string |  |
| `viewerUrl` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `POST /comparisons` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comparison.md) for the provider-specific parameters and requirements.

