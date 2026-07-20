# Constant Contact: Create Contact Custom Field

Creates a contact custom field in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "Favorite Product",
  "type": "date"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "Favorite Product",
    "type": "date"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Custom field label shown in the Constant Contact UI. Example: `Favorite Product`. |
| `type` | string | yes | Data value type for the custom field. Example: `date`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Display and validation metadata object for the custom field. |
| `choices[]` | array<object> | no | Choices array for single_select or multi_select field types. |
| `version` | number | no | Datetime version for date fields (1 legacy string, 2 native date). Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFieldId": "string",
      "label": "string",
      "metadata": {},
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> |  |
| `createdAt` | date |  |
| `customFieldId` | string |  |
| `label` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Constant Contact API, this operation is `POST /contact_custom_fields` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-custom-field.md) for the provider-specific parameters and requirements.

