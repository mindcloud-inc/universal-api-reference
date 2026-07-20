# OkoCRM: Link company entities

Links entities to a company in OkoCRM.

```
PUT https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/link-company-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/link-company-entities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/link-company-entities', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company_id` | number | yes | The OkoCRM company ID. |
| `contact_id` | string | no | A contact ID to link to the company. |
| `lead_id` | string | no | A deal ID to link to the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `POST /companies/[:company_id]/link/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-company-entities.md) for the provider-specific parameters and requirements.

