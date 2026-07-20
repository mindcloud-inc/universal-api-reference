# Revi.io Reviews: Hello World

Tests the Revi.io Reviews API connection.

```
GET https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world?connectionId=$CONNECTION_ID&test=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "test": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world?${params}`, {
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
| `test` | string | yes | A test string echoed back by Revi's hello_world endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Echoed test message returned by Revi. |
| `success` | boolean | Whether the hello_world request succeeded. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `POST /hello_world` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hello-world.md) for the provider-specific parameters and requirements.

