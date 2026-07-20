# SpreadsheetWeb Hub: Update Data Share Link

Updates an existing data share link in SpreadsheetWeb Hub.

```
PUT https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-data-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-data-share-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.dataShareLinkId": "https://example.com",
  "request.applicationId": "string",
  "request.workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-data-share-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.dataShareLinkId": "https://example.com",
    "request.applicationId": "string",
    "request.workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.dataShareLinkId` | string | yes | Identifier of the data share link to update. |
| `request.applicationId` | string | yes | SpreadsheetWeb application identifier that owns the data share link. |
| `request.workspaceId` | string | yes | Workspace identifier that owns the data share link. |

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

Through the native SpreadsheetWeb Hub API, this operation is `POST /datashare/update` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-share-link.md) for the provider-specific parameters and requirements.

