# ServiceTitan: Technician Account Action



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/technician-account-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/technician-account-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "action": "Activate"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/technician-account-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "action": "Activate"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ServiceTitan technician ID. |
| `action` | list<string> | yes | Account action to perform: Activate, Deactivate, SendInvite, or SendPasswordResetLink. One of: `Activate`, `Deactivate`, `SendInvite`, `SendPasswordResetLink`. |
| `licenseType` | list<string> | no | License type to assign to the technician. Required when Action = Activate. One of: `ManagedInstaller`, `ManagedTechnician`, `NonManagedTechnician`. |
| `truckId` | number | no | (Optional) Truck ID to assign to the technician. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST settings/v2/tenant/{{credentials.tenant}}/technicians/:id/account-actions` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/technician-account-action.md) for the provider-specific parameters and requirements.

