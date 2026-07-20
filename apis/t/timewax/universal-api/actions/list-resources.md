# Timewax: List Resources

Retrieves all resource records from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-resources?${params}`, {
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
| `request.isActive` | string | no | Optional. Yes or No. |

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

Through the native Timewax API, this operation is `POST resource/list/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

