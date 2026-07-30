# Viewpoint Vista: Create Job

Adds a Job based on a contract

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "JCCo": 1,
  "Job": "string",
  "Contract": "string",
  "LiabTemplate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "JCCo": 1,
    "Job": "string",
    "Contract": "string",
    "LiabTemplate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `CustRef` | string | no |  |
| `JCCo` | number | yes | Key to jc/jobs(JCCo, Job). 1 to 255. |
| `Job` | string | yes | Key to jc/jobs(JCCo, Job). Length <= 10. |
| `Contract` | string | yes | Key to jc/contracts(JCCo, Contract). Length <= 10. |
| `LiabTemplate` | number | yes | Key to jc/liability_templates(JCCo, LiabTemplate). |
| `LockPhases` | list<string> | no | Optional. If omitted, N will be defaulted. Allowed: Y, N. One of: `N`, `Y`. |
| `ProjectMgr` | number | no | Key to jc/project_managers(JCCo, ProjectMgr). Optional. If omitted, null will be defaulted. |
| `Description` | string | no | Optional. If omitted, it will be defaulted based on Vista defaulting behavior. |
| `BidNumber` | string | no | Optional. If omitted, null will be defaulted. |
| `JobPhone` | string | no | Optional. If omitted, null will be defaulted. |
| `JobFax` | string | no | Optional. If omitted, null will be defaulted. |
| `MailAddress` | string | no | Optional. If omitted, null will be defaulted. |
| `MailCity` | string | no | Optional. If omitted, null will be defaulted. |
| `MailState` | string | no | Optional. If omitted, null will be defaulted. |
| `MailZip` | string | no | Optional. If omitted, null will be defaulted. |
| `MailAddress2` | string | no | Optional. If omitted, null will be defaulted. |
| `ShipAddress` | string | no | Optional. If omitted, null will be defaulted. |
| `ShipCity` | string | no | Optional. If omitted, null will be defaulted. |
| `ShipState` | string | no | Optional. If omitted, null will be defaulted. |
| `ShipZip` | string | no | Optional. If omitted, null will be defaulted. |
| `ShipAddress2` | string | no | Optional. If omitted, null will be defaulted. |
| `TaxCode` | string | no | Key to hq/tax_codes(TaxGroup, TaxCode). TaxGroup will be determined based on JCCo. Optional. If omitted, null will be defaulted. |
| `Notes` | string | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | object | no | Add a property to this object for each user defined field to be set. Property name set to the user defined field name. |

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
| `id` | string |  |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/jobs/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

