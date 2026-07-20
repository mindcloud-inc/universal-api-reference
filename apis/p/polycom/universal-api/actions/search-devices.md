# Polycom: Search Devices

Searches Poly Lens devices and returns inventory details for each result.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-devices?${params}`, {
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
| `variables.params.pageSize` | number | no | Number of devices to return per page. Default: `10`. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.params.nextToken` | string | no | Opaque continuation token returned by the previous device search page. Example: `opaque-page-token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connected": true,
      "id": "string",
      "name": "Ava Chen",
      "serialNumber": "string",
      "softwareVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connected` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `serialNumber` | string |  |
| `softwareVersion` | string |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-devices.md) for the provider-specific parameters and requirements.

