# Viewpoint Vista: Create Contract

Create a contract

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "JCCo": 1,
  "Contract": "string",
  "Department": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "JCCo": 1,
    "Contract": "string",
    "Department": "string"
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
| `Contract` | string | yes | Key to jc/contracts(JCCo, Contract). Length <= 10. |
| `Description` | string | no | Optional. If omitted, it will be defaulted based on Vista defaulting behavior. |
| `Department` | string | yes |  |
| `ContractStatus` | number | no | Allowed: 1, 2, 3 |
| `Notes` | string | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | object | no | Add a property to this object for each user defined field to be set. Property name set to the user defined field name. |
| `ContractItems[]` | array | no |  |
| `Customer` | string | no | Key to ar/customers(CustGroup, Customer). CustGroup will be determined based on JCCo. Optional. If omitted, null will be defaulted. |
| `TaxCode` | string | no |  |

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

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/contracts/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

