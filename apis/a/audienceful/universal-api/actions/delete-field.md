# Audienceful: Delete Field

Deletes an existing custom field from Audienceful.

```
DELETE https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-field?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-field?${params}`, {
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
| `id` | string | yes | Audienceful field id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataName": "Ava Chen",
      "editable": true,
      "id": "string",
      "internal": true,
      "name": "Ava Chen",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataName` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `internal` | boolean |  |
| `name` | string |  |
| `required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Audienceful API, this operation is `DELETE /people/fields/{{id}}/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field.md) for the provider-specific parameters and requirements.

