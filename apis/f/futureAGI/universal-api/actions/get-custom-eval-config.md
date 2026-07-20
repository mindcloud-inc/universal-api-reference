# FutureAGI: Get Custom Eval Config



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-custom-eval-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-custom-eval-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/get-custom-eval-config?${params}`, {
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
| `id` | string | no | Custom eval config ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /tracer/custom-eval-config/:id/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-eval-config.md) for the provider-specific parameters and requirements.

