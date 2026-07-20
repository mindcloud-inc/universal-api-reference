# mintBlue: Get Event Listener

Retrieves an event listener from mintBlue.

```
GET https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-event-listener
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-event-listener?connectionId=$CONNECTION_ID&params.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/get-event-listener?${params}`, {
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
| `params.id` | string | yes | Event listener ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `trigger` | object |  |

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-listener.md) for the provider-specific parameters and requirements.

