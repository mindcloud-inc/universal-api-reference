# Vero: Get Trigger

Retrieves a trigger record from Vero.

```
GET https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger?connectionId=$CONNECTION_ID&id=trigger_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "trigger_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger?${params}`, {
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
| `id` | string | yes | The trigger identifier. Default: `trigger_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Trigger identifier. |
| `object` | string | Resource type. |
| `type` | string | Trigger type. |

## Native endpoint

Through the native Vero API, this operation is `GET /api/v4/triggers/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trigger.md) for the provider-specific parameters and requirements.

