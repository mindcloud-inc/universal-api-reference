# Level: Show Custom Field

Retrieves an existing custom field from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/show-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/show-custom-field?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/show-custom-field?${params}`, {
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
| `id` | string | yes | The ID of the custom field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminOnly": true,
      "id": "string",
      "name": "Ava Chen",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminOnly` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |

## Native endpoint

Through the native Level API, this operation is `GET /custom_fields/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-custom-field.md) for the provider-specific parameters and requirements.

