# Viewpoint Vista: Create Job Phases



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job-phases" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "JCCo": 1,
  "Job": "string",
  "PhaseGroup": 1,
  "Phase": "string",
  "Contract": "string",
  "Item": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job-phases', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "JCCo": 1,
    "Job": "string",
    "PhaseGroup": 1,
    "Phase": "string",
    "Contract": "string",
    "Item": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `JCCo` | number | yes | Key to jc/job_phases(JCCo, Job, PhaseGroup, Phase) and jc/jobs(JCCo, Job). |
| `Job` | string | yes | Job identifier. Maximum 10 characters. |
| `PhaseGroup` | number | yes | Key to jc/job_phases and jc/phases. |
| `Phase` | string | yes | Phase identifier. Maximum 20 characters. |
| `Description` | string | no | Optional. If omitted, null will be defaulted. |
| `Contract` | string | yes | Key to jc/contracts(JCCo, Contract). Maximum 10 characters. |
| `Item` | string | yes | Contract item identifier. Maximum 16 characters. |
| `ProjMinPct` | string | no | Optional percentage value. If omitted, 0 will be defaulted. |
| `ActiveYN` | list<string> | no | Optional. If omitted, Y will be defaulted. One of: `N`, `Y`. |
| `Notes` | string | no | Optional. If omitted, null will be defaulted. |
| `InsCode` | string | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | object | no | Optional Vista user-defined fields, keyed by field name. |
| `CostTypes[]` | array<object> | no | Optional array of cost type objects. Vista applies defaults when omitted; an empty array adds no cost types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Trimble Direct API action identifier. |
| `operation` | string | Operation performed by the Direct API action. |
| `status` | string | Current status of the Direct API action. |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/job_phases/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-phases.md) for the provider-specific parameters and requirements.

