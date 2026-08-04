# Tinybird: Get Environment Variable



```
GET https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-environment-variable?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-environment-variable?${params}`, {
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
| `name` | string | yes | The environment variable name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "edited_by": "string",
      "name": "Ava Chen",
      "type": "string",
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
| `edited_by` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Tinybird API, this operation is `GET v0/variables/:name` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment-variable.md) for the provider-specific parameters and requirements.

