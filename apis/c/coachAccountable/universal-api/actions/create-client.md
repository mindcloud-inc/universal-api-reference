# CoachAccountable: Create Client

Creates a client in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `email` | string | yes |  |
| `homePhone` | string | no |  |
| `cellPhone` | string | no |  |
| `workPhone` | string | no |  |
| `gender` | list | no | One of: `F`, `M`, `U`. Default: `U`. |
| `timezone` | string | no | The timezone of the new Client. If not provided, defaults to match her Coach's timezone. |
| `address` | string | no | The client's street address. |
| `city` | string | no | The client's city. |
| `state` | string | no | The client's state. |
| `zip` | string | no | The client's ZIP or postal code. |
| `onDuplicateEmail` | list | no | What to do if a Client with the supplied email already exists. One of: `A`, `E`, `S`. Default: `S`. |
| `upgradeIfNeeded` | boolean | no | If alread at the limit, upgrade the account to make space for the new Client. If false, the call will return failure when there is no space. Default: `true`. |
| `sendInvite` | boolean | no | Send true if the new client should be sent an invite email immediately. Default: `false`. |
| `inviteSubject` | string | no | Subject line of the invite email to be sent (if opted for). If not included, will use template setting. |
| `inviteMessage` | string | no | Body of the invite email to be sent (if opted for], [magicLink] is required. If not included, will use template setting. |
| `profileExtra` | string | no | Any additional information you'd like to have on file, accessible at-a-glance. |
| `appointmentScheduleRule` | list | no | One of: `ABE`, `AUE`, `D`, `NA`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ClientID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ClientID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

