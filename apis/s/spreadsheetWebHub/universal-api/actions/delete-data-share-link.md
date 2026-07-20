# SpreadsheetWeb Hub: Delete Data Share Link

Deletes an existing data share link from SpreadsheetWeb Hub.

```
DELETE https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-data-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-data-share-link?connectionId=$CONNECTION_ID&request.dataShareLinkId=https%3A%2F%2Fexample.com&request.applicationId=string&request.workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.dataShareLinkId": "https://example.com",
  "request.applicationId": "string",
  "request.workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/delete-data-share-link?${params}`, {
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
| `request.dataShareLinkId` | string | yes | Identifier of the data share link to delete. |
| `request.applicationId` | string | yes | SpreadsheetWeb application identifier that owns the data share link. |
| `request.workspaceId` | string | yes | Workspace identifier that owns the data share link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /datashare/delete` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-data-share-link.md) for the provider-specific parameters and requirements.

