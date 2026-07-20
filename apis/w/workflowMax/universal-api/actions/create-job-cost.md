# WorkflowMax: Create Job Cost



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-cost" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-cost', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobIdentifier` | string | yes | The WorkflowMax job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": true,
      "billable": true,
      "costCode": "string",
      "costName": "Ava Chen",
      "costUUID": "string",
      "createdAt": "string",
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "date": "string",
      "note": "string",
      "order": 1,
      "phase": {
        "name": "Ava Chen",
        "uuid": "string"
      },
      "quantity": 1,
      "supplier": {
        "name": "Ava Chen",
        "uuid": "string"
      },
      "type": "string",
      "unitCost": 1,
      "unitPrice": 1,
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | boolean | Indicate whether the job cost is actual or estimated. |
| `billable` | boolean | Indicate whether the job cost is billable or not. |
| `costCode` | string | The code of the job cost. |
| `costName` | string | The name of the job cost. |
| `costUUID` | string | The unique identifier of the cost as managed in the cost admin which is associated with the job cost. |
| `createdAt` | string | The UTC timestamp indicating when the job cost was created. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `date` | string | The date of the job cost. |
| `note` | string | The note of the job cost. |
| `order` | number | Indicate the order of the job cost as in the job. |
| `phase.name` | string | The name of the phase associated to the job cost. |
| `phase.uuid` | string | The unique identifier of the phase associated to the job cost. |
| `quantity` | number | The quantity of the job cost. |
| `supplier.name` | string | The name of the supplier associated to the job cost. |
| `supplier.uuid` | string | The unique identifier of the supplier associated to the job cost. |
| `type` | string | The type of the job cost. Possible value: Service or Stock. |
| `unitCost` | number | The unit cost of the job cost. |
| `unitPrice` | number | The unit price of the job cost. |
| `updatedAt` | string | The UTC timestamp indicating when the job cost was last updated. |
| `uuid` | string | The unique identifier of the job cost. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/jobs/{identifier}/costs` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-cost.md) for the provider-specific parameters and requirements.

