# Coast: Update Person By ID



```
PUT https://connect.mindcloud.co/v1/universal/coast/latest/actions/updateperson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coast/latest/actions/updateperson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/updateperson', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | yes | Coast person ID of the person to update. |
| `active` | boolean | no | Whether the person is active in Coast. |
| `firstName` | string | no | Updated first name for the person. |
| `lastName` | string | no | Updated last name for the person. |
| `email` | string | no | Updated email address for the person. |
| `mobilePhone` | string | no | Updated mobile phone number for the person. |
| `locationId` | string | no | Coast location ID to assign to the person. |
| `departmentId` | string | no | Coast department ID to assign to the person. |
| `roleId` | string | no | Coast role ID to assign to the person. |
| `access` | string | no | Updated access settings for the person. |
| `policyId` | string | no | Coast policy ID to assign to the person. |
| `security` | string | no | Updated security settings for the person. |
| `assignedVehicleId` | string | no | Coast vehicle ID to assign to the person. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `PATCH /v2/people/:personId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/updateperson.md) for the provider-specific parameters and requirements.

