# Timewax: Get Resource

Retrieves a resource from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-resource?connectionId=$CONNECTION_ID&request.resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-resource?${params}`, {
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
| `request.resource` | string | yes | Required. Name, full name, or email of the resource. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "isActive": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Resource code. |
| `email` | string | Resource email address. |
| `fullName` | string | Resource full name. |
| `isActive` | boolean | Whether the resource is active. |

## Native endpoint

Through the native Timewax API, this operation is `POST resource/get/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

