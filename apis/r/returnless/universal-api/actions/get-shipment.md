# Returnless: Get Shipment

Retrieves a shipment from Returnless.

```
GET https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-shipment?connectionId=$CONNECTION_ID&shipment=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipment": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-shipment?${params}`, {
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
| `shipment` | string | yes | The unique identifier of the shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Shipment payload retrieved by ID. |
| `meta` | object | Execution metadata. |

## Native endpoint

Through the native Returnless API, this operation is `GET /2025-01/shipments/{shipment}` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

