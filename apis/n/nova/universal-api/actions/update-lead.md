# Nova: Update Lead



```
PUT https://connect.mindcloud.co/v1/universal/nova/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nova/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "origin_crm_id": "crm-123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nova/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "origin_crm_id": "crm-123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `origin_crm_id` | string | yes | External CRM lead identifier used by Nova to locate the lead to update. Default: `crm-123`. Example: `crm-123`. |
| `phone_number_concatenated` | string | no | Updated lead phone number. Example: `+33777777777`. |
| `firstname` | string | no | Updated lead first name. Example: `John`. |
| `lastname` | string | no | Updated lead last name. Example: `Doe`. |
| `email` | string | no | Updated lead email address. Example: `john.doe@example.com`. |
| `statut` | string | no | Updated Nova lead status label. Example: `Intéressé`. |
| `assigned_to` | string | no | Updated Nova user ID assigned to the lead. Example: `10537`. |
| `commentaire` | string | no | Updated lead comment. Example: `Lead contacted`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Raw textual result returned by Nova after the lead update request. |

## Native endpoint

Through the native Nova API, this operation is `PUT /rt/update/lead` (base URL `https://app.n0va.com/v1/la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

