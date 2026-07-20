# RD Station Marketing: Update Contact Default Funnel by UUID or Email



```
PUT https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-default-funnel-by-uuid-or-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-default-funnel-by-uuid-or-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "email",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-default-funnel-by-uuid-or-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "email",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_owner_email` | string | no | Email do dono do contato. |
| `identifier` | list<string> | yes | Identifier type in path (uuid or email). One of: `email`, `uuid`. |
| `lifecycle_stage` | string | no | Etapa do ciclo de vida. |
| `opportunity` | boolean | no | Indica se o contato é oportunidade. |
| `value` | string | yes | Identifier value in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactOwnerEmail": "ava@example.com",
      "fit": 1,
      "interest": 1,
      "lifecycleStage": "string",
      "opportunity": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactOwnerEmail` | string |  |
| `fit` | number |  |
| `interest` | number |  |
| `lifecycleStage` | string |  |
| `opportunity` | boolean |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `PUT /platform/contacts/:identifier::value/funnels/default` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-default-funnel-by-uuid-or-email.md) for the provider-specific parameters and requirements.

