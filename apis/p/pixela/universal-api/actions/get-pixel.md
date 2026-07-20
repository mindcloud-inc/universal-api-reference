# Pixela: Get Pixel

Retrieves a pixel from a Pixela graph by date.

```
GET https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-pixel?connectionId=$CONNECTION_ID&username=Ava%20Chen&graph_id=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "graph_id": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-pixel?${params}`, {
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
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Pixela graph identifier. |
| `date` | string | yes | Pixel date in yyyyMMdd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "optionalData": "string",
      "quantity": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `optionalData` | string |  |
| `quantity` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `GET /v1/users/:username/graphs/:graphID/:yyyyMMdd` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pixel.md) for the provider-specific parameters and requirements.

