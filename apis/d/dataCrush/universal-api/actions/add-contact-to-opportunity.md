# DataCrush: Add Contact To Opportunity

Adds a contact to an opportunity in DataCrush.

```
PUT https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/add-contact-to-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/add-contact-to-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunity_key": "string",
  "contact_key": "string",
  "role": "string",
  "main": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/add-contact-to-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunity_key": "string",
    "contact_key": "string",
    "role": "string",
    "main": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunity_key` | string | yes | Opportunity key to update. |
| `contact_key` | string | yes | Contact key to associate. |
| `role` | string | yes | Contact role in the opportunity. |
| `main` | string | yes | Whether the contact is the main contact: 1 or 0. Example: `1`. |

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
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /crm/opportunity/contact-add` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-opportunity.md) for the provider-specific parameters and requirements.

