# Constant Contact: Delete Contact Custom Field

Deletes a contact custom field from Constant Contact.

```
DELETE https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-custom-field?connectionId=$CONNECTION_ID&customFieldId=04fe9a-a579-43c5-bb1a-58ed29bf0a6a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customFieldId": "04fe9a-a579-43c5-bb1a-58ed29bf0a6a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-custom-field?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldId` | string | yes | The ID that uniquely identifies the custom field to delete. Example: `04fe9a-a579-43c5-bb1a-58ed29bf0a6a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `DELETE /contact_custom_fields/:custom_field_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-custom-field.md) for the provider-specific parameters and requirements.

