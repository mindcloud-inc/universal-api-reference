# ActiveCampaign: Create Custom Field Value

Creates a custom field value in ActiveCampaign.

```
POST https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-custom-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-custom-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldValue.contact": "string",
  "fieldValue.field": "string",
  "fieldValue.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-custom-field-value', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `fieldValue` | object | no |  |
| `fieldValue.contact` | string | yes |  |
| `fieldValue.field` | string | yes |  |
| `fieldValue.value` | string | yes |  |
| `useDefaults` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /fieldValues` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field-value.md) for the provider-specific parameters and requirements.

