# ActiveCampaign: Update Custom Field Value For Contact

Updates a contact custom field value in ActiveCampaign.

```
PUT https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-custom-field-value-for-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-custom-field-value-for-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "fieldValue.contact": "string",
  "fieldValue.field": "string",
  "fieldValue.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-custom-field-value-for-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "fieldValue.contact": "string",
    "fieldValue.field": "string",
    "fieldValue.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The field value ID. |
| `fieldValue` | object | no |  |
| `fieldValue.contact` | string | yes |  |
| `fieldValue.field` | string | yes |  |
| `fieldValue.value` | string | yes |  |
| `useDefaults` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `PUT /fieldValues/:id` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field-value-for-contact.md) for the provider-specific parameters and requirements.

