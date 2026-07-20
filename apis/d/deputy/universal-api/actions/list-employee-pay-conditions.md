# Deputy: List Employee Pay Conditions

Retrieves employee pay conditions from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employee-pay-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employee-pay-conditions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employee-pay-conditions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "Active": true,
      "Config": "string",
      "Contract": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "EffectiveDate": "2026-05-07T12:00:00.000Z",
      "EmployeeId": 1,
      "EmpType": 1,
      "Id": 1,
      "Modified": "2026-05-07T12:00:00.000Z",
      "PayPeriod": 1,
      "PayPoint": 1,
      "StartDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `Active` | boolean |  |
| `Config` | string |  |
| `Contract` | number |  |
| `Created` | date |  |
| `EffectiveDate` | date |  |
| `EmployeeId` | number |  |
| `EmpType` | number |  |
| `Id` | number |  |
| `Modified` | date |  |
| `PayPeriod` | number |  |
| `PayPoint` | number |  |
| `StartDate` | date |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/EmployeeAgreement/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-pay-conditions.md) for the provider-specific parameters and requirements.

