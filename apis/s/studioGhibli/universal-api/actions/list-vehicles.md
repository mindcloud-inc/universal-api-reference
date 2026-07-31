# Studio Ghibli: List Vehicles



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-vehicles?${params}`, {
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
| `fields` | string | no | Optional comma-separated list of response fields documented by the provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "films": [
        "string"
      ],
      "id": "string",
      "length": "string",
      "name": "Ava Chen",
      "pilot": "string",
      "url": "https://example.com",
      "vehicle_class": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Vehicle description. |
| `films` | array<string> | Related film URLs. |
| `id` | string | Provider UUID. |
| `length` | string | Provider length string. |
| `name` | string | Vehicle name. |
| `pilot` | string | Related person URL. |
| `url` | string | Canonical resource URL. |
| `vehicle_class` | string | Native vehicle class. |

## Native endpoint

Through the native Studio Ghibli API, this operation is `GET /vehicles` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

