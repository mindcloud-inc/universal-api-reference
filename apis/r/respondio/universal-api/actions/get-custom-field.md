# respond.io: Get Custom Field

Retrieves a custom field from respond.io.

```
GET https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-custom-field?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-custom-field?${params}`, {
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
| `id` | string | yes | Custom field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "dataType": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native respond.io API, this operation is `GET /space/custom_field/:id` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-field.md) for the provider-specific parameters and requirements.

