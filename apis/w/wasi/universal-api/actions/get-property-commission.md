# Wasi: Get Property Commission

Retrieves a property's commission details from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property-commission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property-commission?connectionId=$CONNECTION_ID&property_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "property_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property-commission?${params}`, {
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
| `property_id` | number | yes | Wasi property ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "commission": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Provider error code when present. |
| `commission` | number | Commission value when Wasi returns it. |
| `message` | string | Provider message when the property cannot be resolved. |
| `status` | string | Wasi operation status. |

## Native endpoint

Through the native Wasi API, this operation is `GET /property/get-commission/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-commission.md) for the provider-specific parameters and requirements.

