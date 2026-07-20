# HR Partner: Get Timesheet



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-timesheet?connectionId=$CONNECTION_ID&employee=string&sequence=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "string",
  "sequence": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-timesheet?${params}`, {
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
| `employee` | string | yes | Employee code to fetch a single timesheet for. |
| `sequence` | string | yes | Exact timesheet sequence label, such as Mon, 01 Jan 2024 to Sun, 07 Jan 2024. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvingUser": "string",
      "closingDate": "2026-05-07T12:00:00.000Z",
      "details": [
        {}
      ],
      "employee": {},
      "endDate": "2026-05-07T12:00:00.000Z",
      "entryMethod": "string",
      "frequency": "string",
      "id": 1,
      "isApproved": "string",
      "isExported": "string",
      "isLocked": "string",
      "rounding": "string",
      "roundTo": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "template": "string",
      "totalTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvingUser` | string |  |
| `closingDate` | date |  |
| `details` | array<object> |  |
| `employee` | object |  |
| `endDate` | date |  |
| `entryMethod` | string |  |
| `frequency` | string |  |
| `id` | number |  |
| `isApproved` | string |  |
| `isExported` | string |  |
| `isLocked` | string |  |
| `rounding` | string |  |
| `roundTo` | number |  |
| `startDate` | date |  |
| `status` | string |  |
| `template` | string |  |
| `totalTime` | number |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /singletimesheet` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet.md) for the provider-specific parameters and requirements.

