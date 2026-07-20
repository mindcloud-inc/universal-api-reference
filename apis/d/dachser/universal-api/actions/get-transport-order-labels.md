# Dachser: Get Transport Order Labels

Retrieves labels for an existing transport order in Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-transport-order-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-transport-order-labels?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-transport-order-labels?${params}`, {
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
| `id` | number | yes | DACHSER transport order ID. |
| `labelFormat` | string | no | Label format. Use P for PDF or Z for Zebra Printer Language. Default: `P`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "label": "string",
      "links": [
        {}
      ],
      "messages": [
        "string"
      ],
      "ssccs": [
        "string"
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `label` | string |  |
| `links` | array<object> |  |
| `messages` | array<string> |  |
| `ssccs` | array<string> |  |
| `state` | string |  |

## Native endpoint

Through the native Dachser API, this operation is `POST /rest/v2/transportorders/{id}/labels` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transport-order-labels.md) for the provider-specific parameters and requirements.

