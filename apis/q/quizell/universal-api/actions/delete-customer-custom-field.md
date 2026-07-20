# Quizell: Delete Customer Custom Field

Deletes a customer custom field from Quizell.

```
DELETE https://connect.mindcloud.co/v1/universal/quizell/latest/actions/delete-customer-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/delete-customer-custom-field?connectionId=$CONNECTION_ID&fieldId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/delete-customer-custom-field?${params}`, {
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
| `fieldId` | number | yes | ID of the custom field to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Quizell API, this operation is `DELETE /customers/custom_fields/delete/:field_id` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-custom-field.md) for the provider-specific parameters and requirements.

