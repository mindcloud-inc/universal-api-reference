# Paylocity: Get Employee Punch Detail



```
GET https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-punch-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paylocity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-punch-detail?connectionId=$CONNECTION_ID&companyId=string&employeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string",
  "employeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-punch-detail?${params}`, {
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
| `companyId` | string | yes |  |
| `employeeId` | string | yes |  |
| `relativeStart` | string | no |  |
| `relativeEnd` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeNumber": "string",
      "companyId": "string",
      "employeeId": "string",
      "relativeEnd": "2026-05-07T12:00:00.000Z",
      "relativeStart": "2026-05-07T12:00:00.000Z",
      "segments": [
        {
          "costCenters": [
            {
              "code": "string",
              "costCenterId": 1,
              "id": "string",
              "isActive": true,
              "level": 1,
              "name": "Ava Chen"
            }
          ],
          "date": "2026-05-07T12:00:00.000Z",
          "durationSeconds": 1,
          "earnings": 1,
          "origin": "string",
          "punchID": "string",
          "punchType": "string",
          "relativeEnd": "2026-05-07T12:00:00.000Z",
          "relativeOriginalEnd": "2026-05-07T12:00:00.000Z",
          "relativeOriginalStart": "2026-05-07T12:00:00.000Z",
          "relativeStart": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeNumber` | string |  |
| `companyId` | string |  |
| `employeeId` | string |  |
| `relativeEnd` | date |  |
| `relativeStart` | date |  |
| `segments[].costCenters[].code` | string |  |
| `segments[].costCenters[].costCenterId` | number |  |
| `segments[].costCenters[].id` | string |  |
| `segments[].costCenters[].isActive` | boolean |  |
| `segments[].costCenters[].level` | number |  |
| `segments[].costCenters[].name` | string |  |
| `segments[].date` | date |  |
| `segments[].durationSeconds` | number |  |
| `segments[].earnings` | number |  |
| `segments[].origin` | string |  |
| `segments[].punchID` | string |  |
| `segments[].punchType` | string |  |
| `segments[].relativeEnd` | date |  |
| `segments[].relativeOriginalEnd` | date |  |
| `segments[].relativeOriginalStart` | date |  |
| `segments[].relativeStart` | date |  |

## Native endpoint

Through the native Paylocity API, this operation is `GET apiHub/time/v1/companies/:companyId/employees/:employeeId/punchDetails` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-punch-detail.md) for the provider-specific parameters and requirements.

