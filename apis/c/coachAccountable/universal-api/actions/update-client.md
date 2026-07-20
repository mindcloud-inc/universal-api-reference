# CoachAccountable: Update Client

Updates a client in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `homePhone` | string | no |  |
| `cellPhone` | string | no |  |
| `workPhone` | string | no |  |
| `timezone` | string | no | The timezone of the Client. |
| `address` | string | no | The client's street address. |
| `city` | string | no | The client's city. |
| `state` | string | no | The client's state. |
| `zip` | string | no | The client's ZIP or postal code. |
| `appointmentScheduleRule` | list | no | One of: `ABE`, `AUE`, `D`, `NA`. Default: `D`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

