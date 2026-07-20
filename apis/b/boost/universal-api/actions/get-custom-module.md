# Boost: Get Custom Module

Retrieves a custom module from Boost by ID.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-custom-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-custom-module?connectionId=$CONNECTION_ID&customModuleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customModuleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-custom-module?${params}`, {
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
| `customModuleId` | number | yes | Boost.space custom module ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `description` | string | Custom module description. |
| `id` | number | Custom module ID. |
| `name` | string | Custom module name. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Boost API, this operation is `GET /custom-module/{customModuleId}` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-module.md) for the provider-specific parameters and requirements.

