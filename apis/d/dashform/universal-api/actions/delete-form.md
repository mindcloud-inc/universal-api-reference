# Dashform: Delete Form

Deletes a form from Dashform.

```
DELETE https://connect.mindcloud.co/v1/universal/dashform/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/delete-form?connectionId=$CONNECTION_ID&id=form_123%20or%20public_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "form_123 or public_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashform/latest/actions/delete-form?${params}`, {
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
| `id` | string | yes | Dashform form ID or public ID. Example: `form_123 or public_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the form was deleted |

## Native endpoint

Through the native Dashform API, this operation is `DELETE /api/v1/forms/:id` (base URL `https://getaiform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

