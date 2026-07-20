# Flexopus: List Location Bookables

Retrieves bookables for a specific Flexopus location.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookables?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookables?${params}`, {
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
| `locationId` | number | yes | The ID of the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": 1,
          "name": "Ava Chen",
          "status": 1,
          "tags": [
            "string"
          ],
          "type": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].status` | number |  |
| `data[].tags` | array<string> |  |
| `data[].type` | number |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /locations/:location_id/bookables` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-location-bookables.md) for the provider-specific parameters and requirements.

