# Constant Contact: Update Contact Custom Field

Updates a contact custom field in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFieldId": "04fe9a-a579-43c5-bb1a-58ed29bf0a6a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFieldId": "04fe9a-a579-43c5-bb1a-58ed29bf0a6a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldId` | string | yes | The ID that uniquely identifies the custom field to update. Example: `04fe9a-a579-43c5-bb1a-58ed29bf0a6a`. |
| `label` | string | no | The custom field label to display. Example: `Favorite color`. |
| `choices[]` | array<object> | no | Array of choice objects for single_select or multi_select fields. |

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

Through the native Constant Contact API, this operation is `PUT /contact_custom_fields/:custom_field_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-custom-field.md) for the provider-specific parameters and requirements.

