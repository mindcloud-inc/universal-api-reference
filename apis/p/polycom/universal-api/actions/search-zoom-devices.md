# Polycom: Search Zoom Devices

Searches Poly Lens devices whose active application is Zoom.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-zoom-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-zoom-devices?connectionId=$CONNECTION_ID&variables.params.sort.fields%5B0%5D.name=id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.params.sort.fields[0].name": "id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-zoom-devices?${params}`, {
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
| `variables.params.pageSize` | number | no | Maximum number of devices to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.params.sort.fields[0].name` | string | yes | Sort field name. Default: `id`. |
| `variables.params.nextToken` | string | no | Opaque token for the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeApplicationName": "Ava Chen",
      "activeApplicationVersion": "string",
      "connected": true,
      "connections": [
        {
          "connected": true,
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "hardwareModel": "string",
      "id": "string",
      "name": "Ava Chen",
      "room": {
        "floor": "string",
        "name": "Ava Chen"
      },
      "serialNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeApplicationName` | string |  |
| `activeApplicationVersion` | string |  |
| `connected` | boolean |  |
| `connections[].connected` | boolean |  |
| `connections[].id` | string |  |
| `connections[].name` | string |  |
| `hardwareModel` | string |  |
| `id` | string |  |
| `name` | string |  |
| `room.floor` | string |  |
| `room.name` | string |  |
| `serialNumber` | string |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-zoom-devices.md) for the provider-specific parameters and requirements.

