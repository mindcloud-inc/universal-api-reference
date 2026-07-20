# AssessTEAM: Get Timesheet Data

Retrieves recorded timesheet data from AssessTEAM.

```
GET https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-timesheet-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-timesheet-data?connectionId=$CONNECTION_ID&month=string&personCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "month": "string",
  "personCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-timesheet-data?${params}`, {
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
| `month` | string | yes | Month, for example Apr-2026. |
| `personCode` | string | yes | Unique person code, for example 1001. |
| `projectName` | string | no | Project name to narrow the result. |
| `date` | string | no | Date for day mode, for example 5-Mar-2025. |
| `dayWiseTimesheet` | boolean | no | Show day-wise timesheet data when true. |
| `projectWiseTimesheet` | boolean | no | Show project-wise timesheet data with comments when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "personID": 1,
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `personID` | number |  |
| `statusCode` | number |  |

## Native endpoint

Through the native AssessTEAM API, this operation is `GET /timesheet/gettimesheetdata` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet-data.md) for the provider-specific parameters and requirements.

