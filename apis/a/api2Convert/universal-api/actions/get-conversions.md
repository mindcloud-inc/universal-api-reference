# Api2Convert: Get Conversions

Retrieves valid conversion types from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-conversions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-conversions?${params}`, {
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
| `category` | string | no | Filter available conversions by category. |
| `target` | string | no | Filter available conversions by target format. |
| `page` | string | no | Page number for paginated conversion results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": 1,
      "options": {},
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Conversion category. |
| `id` | number | Identifier of the supported conversion. |
| `options` | object | Available options for the conversion. |
| `target` | string | Target conversion format. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /conversions` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversions.md) for the provider-specific parameters and requirements.

