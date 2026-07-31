# Studio Ghibli: Get Person by ID



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-person-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-person-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-person-by-id?${params}`, {
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
      "age": "string",
      "eye_color": "string",
      "films": [
        "string"
      ],
      "gender": "string",
      "hair_color": "string",
      "id": "string",
      "name": "Ava Chen",
      "species": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string | Provider age value. |
| `eye_color` | string | Native eye-colour value. |
| `films` | array<string> | Related film URLs. |
| `gender` | string | Provider gender value. |
| `hair_color` | string | Native hair-colour value. |
| `id` | string | Provider UUID. |
| `name` | string | Person name. |
| `species` | string | Related species URL. |
| `url` | string | Canonical resource URL. |

## Native endpoint

Through the native Studio Ghibli API, this operation is `GET /people/:id` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-id.md) for the provider-specific parameters and requirements.

