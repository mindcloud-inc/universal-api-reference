# SimpleKPI: Get Group

Retrieves a group record from SimpleKPI.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-group?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-group?${params}`, {
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
| `id` | number | yes | SimpleKPI group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "sort_order": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `name` | string |  |
| `sort_order` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET groups/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

