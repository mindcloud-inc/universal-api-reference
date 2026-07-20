# MyHR: Update Company Time Off Reason



```
PUT https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-company-time-off-reason
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-company-time-off-reason" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyTimeOffReasonPid": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-company-time-off-reason', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyTimeOffReasonPid": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyTimeOffReasonPid` | string | yes | The company time off reason PID. |
| `label` | string | yes | The updated company time off reason label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "label": "string",
      "object": "string",
      "pid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `label` | string |  |
| `object` | string |  |
| `pid` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `PUT /company_timeoff_reasons/:company_timeoff_reason_pid` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-time-off-reason.md) for the provider-specific parameters and requirements.

