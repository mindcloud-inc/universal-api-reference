# Studio Ghibli: Get Species by ID



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-species-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-species-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-species-by-id?${params}`, {
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
      "classification": "string",
      "eye_colors": "string",
      "films": [
        "string"
      ],
      "hair_colors": "string",
      "id": "string",
      "name": "Ava Chen",
      "people": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string | Species classification. |
| `eye_colors` | string | Native eye-colours value. |
| `films` | array<string> | Related film URLs. |
| `hair_colors` | string | Native hair-colours value. |
| `id` | string | Provider UUID. |
| `name` | string | Species name. |
| `people` | array<string> | Related person URLs. |
| `url` | string | Canonical resource URL. |

## Native endpoint

Through the native Studio Ghibli API, this operation is `GET /species/:id` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-species-by-id.md) for the provider-specific parameters and requirements.

