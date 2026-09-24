# ADP: List Worker Leaves



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-leaves
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-leaves?connectionId=$CONNECTION_ID&aoid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aoid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-leaves?${params}`, {
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
| `aoid` | string | yes | The ADP associate object identifier for the worker whose leave records should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associateOID": "string",
      "leaves": [
        {
          "effectiveDateTime": "string",
          "leaveAbsence": {
            "expectedEndDateTime": "string",
            "leaveTypeCode": {
              "codeValue": "string"
            },
            "paymentStatusCode": {
              "codeValue": "string"
            },
            "startDateTime": "string"
          },
          "leaveReturn": {
            "returnStatus": {
              "returnStatusCode": {
                "codeValue": "string"
              }
            }
          }
        }
      ],
      "workAssignmentID": "string",
      "workerID": {
        "idValue": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associateOID` | string |  |
| `leaves[].effectiveDateTime` | string |  |
| `leaves[].leaveAbsence.expectedEndDateTime` | string |  |
| `leaves[].leaveAbsence.leaveTypeCode.codeValue` | string |  |
| `leaves[].leaveAbsence.paymentStatusCode.codeValue` | string |  |
| `leaves[].leaveAbsence.startDateTime` | string |  |
| `leaves[].leaveReturn.returnStatus.returnStatusCode.codeValue` | string |  |
| `workAssignmentID` | string |  |
| `workerID.idValue` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET hr/v2/workers/:aoid/leaves` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worker-leaves.md) for the provider-specific parameters and requirements.

