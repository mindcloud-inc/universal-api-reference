# SpreadsheetWeb Hub: List Data Share Links

Retrieves data share links from SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-data-share-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-data-share-links?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string&applicationId=string&dataId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string",
  "applicationId": "string",
  "dataId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-data-share-links?${params}`, {
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
| `workspaceId` | string | yes | SpreadsheetWeb workspace UUID. |
| `applicationId` | string | yes | SpreadsheetWeb application UUID. |
| `dataId` | number | yes | SpreadsheetWeb record data identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessedCount": 1,
      "actionType": 1,
      "applicationId": "string",
      "createdByClientId": 1,
      "createdByUserId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataShareLinkId": "https://example.com",
      "dataShareToken": "string",
      "expirationTime": "2026-05-07T12:00:00.000Z",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "recordId": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessedCount` | number |  |
| `actionType` | number |  |
| `applicationId` | string |  |
| `createdByClientId` | number |  |
| `createdByUserId` | string |  |
| `creationDate` | date |  |
| `dataShareLinkId` | string |  |
| `dataShareToken` | string |  |
| `expirationTime` | date |  |
| `modificationDate` | date |  |
| `recordId` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /datashare/list/:workspaceId/:applicationId/:dataId` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-share-links.md) for the provider-specific parameters and requirements.

