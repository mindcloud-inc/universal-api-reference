# Apilio: Get Boolean Variable



```
GET https://connect.mindcloud.co/v1/universal/apilio/latest/actions/get-boolean-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/get-boolean-variable?connectionId=$CONNECTION_ID&uuid=a40f21df-7707-4898-9688-69bf1f8dd184" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apilio/latest/actions/get-boolean-variable?${params}`, {
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
| `uuid` | string | yes | The UUID of the boolean variable to retrieve. Default: `a40f21df-7707-4898-9688-69bf1f8dd184`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |
| `value` | boolean |  |

## Native endpoint

Through the native Apilio API, this operation is `GET /api/v1/boolean_variables/{{uuid}}` (base URL `https://api.apilio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-boolean-variable.md) for the provider-specific parameters and requirements.

