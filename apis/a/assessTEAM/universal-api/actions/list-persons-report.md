# AssessTEAM: List Persons Report

Retrieves the persons report from AssessTEAM.

```
GET https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-persons-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-persons-report?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-persons-report?${params}`, {
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
| `fromDate` | string | yes | From month of the date range, for example Jan-2026. |
| `toDate` | string | yes | To month of the date range, for example Apr-2026. |
| `display` | string | no | Display mode, for example 3. Default: `1`. |
| `projectName` | string | no | Project name, for example Acme Web Site. |
| `teamName` | string | no | Team name, for example Testing Team. |
| `personName` | string | no | Person name, for example Jon Doe. |
| `peer` | boolean | no | Include peer evaluations. |
| `upward` | boolean | no | Include upward evaluations. |
| `self` | boolean | no | Include self evaluations. Default: `true`. |
| `downward` | boolean | no | Include downward evaluations. |
| `customer` | boolean | no | Include customer evaluations. |
| `undefinedLevel` | boolean | no | Include undefined evaluation level. |

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

Through the native AssessTEAM API, this operation is `GET /reports/persons` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-persons-report.md) for the provider-specific parameters and requirements.

