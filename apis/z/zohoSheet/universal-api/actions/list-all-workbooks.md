# Zoho Sheet: List All Workbooks

Retrieves all workbooks from Zoho Sheet.

```
GET https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks?${params}`, {
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
| `startIndex` | number | no | Optional Parameter. This parameter can be used to get a few resources if there are too many. |
| `count` | number | no | Optional Parameter. It denotes the number of resources in response. |
| `sortOption` | string | no | Optional Parameter. Supported options are 'recently_opened', 'recently_modified', 'recently_created', 'ascending', and 'descending'. Default option is 'recently_created'. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "method": "string",
      "resourceCount": 1,
      "resourceEndIndex": 1,
      "resourceStartIndex": 1,
      "status": "string",
      "workbooks": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `method` | string |  |
| `resourceCount` | number |  |
| `resourceEndIndex` | number |  |
| `resourceStartIndex` | number |  |
| `status` | string |  |
| `workbooks[]` | array<object> |  |
| `workbooks[].createdBy` | string |  |
| `workbooks[].createdTime` | string |  |
| `workbooks[].lastModifiedTime` | string |  |
| `workbooks[].permission` | number |  |
| `workbooks[].resourceId` | string |  |
| `workbooks[].workbookName` | string |  |
| `workbooks[].workbookUrl` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /workbooks` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-workbooks.md) for the provider-specific parameters and requirements.

