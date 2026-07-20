# Timewax: Get Client

Retrieves a client from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-client?connectionId=$CONNECTION_ID&request.company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-client?${params}`, {
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
| `request.company` | string | yes | Required. Code or name of the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "name": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Client code. |
| `name` | string | Client name. |
| `website` | string | Client website. |

## Native endpoint

Through the native Timewax API, this operation is `POST company/get/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

