# Studio Ghibli: Get Vehicle by ID



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-vehicle-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-vehicle-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-vehicle-by-id?${params}`, {
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
| `id` | string | yes | Resource UUID documented by the provider. |
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

Through the native Studio Ghibli API, this operation is `GET /vehicles/:id` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vehicle-by-id.md) for the provider-specific parameters and requirements.

