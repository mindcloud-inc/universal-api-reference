# SpreadsheetWeb Hub: Get Calculation Progress

Retrieves calculation progress from SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-calculation-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-calculation-progress?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-calculation-progress?${params}`, {
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
| `request` | string | no | Async calculation progress UUID. |
| `keys` | object | no | Calculation key envelope. |
| `keys.applicationId` | string | no | SpreadsheetWeb application UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "entryKey": "string",
      "isError": true,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "maximum": 1,
      "message": "string",
      "minimum": 1,
      "position": 1,
      "progressData": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `entryKey` | string |  |
| `isError` | boolean |  |
| `lastUpdate` | date |  |
| `maximum` | number |  |
| `message` | string |  |
| `minimum` | number |  |
| `position` | number |  |
| `progressData` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /calculations/getprogressstate` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calculation-progress.md) for the provider-specific parameters and requirements.

