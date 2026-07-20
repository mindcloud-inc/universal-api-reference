# AssessTEAM: List Evaluations Report

Retrieves the evaluations report from AssessTEAM.

```
GET https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-evaluations-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-evaluations-report?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-evaluations-report?${params}`, {
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
| `projectName` | string | no | Project name, for example Acme web site. |
| `teamName` | string | no | Team name, for example Testing team. |
| `personName` | string | no | Person name, for example Jon doe. |
| `personTag` | string | no | Person tag, for example tag1. |
| `peer` | boolean | no | Include evaluations from peer reviews. |
| `upward` | boolean | no | Include evaluations from upward reviews. |
| `self` | boolean | no | Include evaluations from self reviews. Default: `true`. |
| `downward` | boolean | no | Include evaluations from downward reviews. |
| `customer` | boolean | no | Include customer satisfaction evaluations. |
| `undefinedLevel` | boolean | no | Include undefined evaluation levels. |

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

Through the native AssessTEAM API, this operation is `GET /reports/evaluations` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-evaluations-report.md) for the provider-specific parameters and requirements.

