# Launch Library 2: Get Astronaut



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-astronaut
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-astronaut?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-astronaut?${params}`, {
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
| `id` | string | yes | Astronaut ID from Launch Library 2. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "agency": {
        "name": "Ava Chen"
      },
      "date_of_birth": "2026-05-07T12:00:00.000Z",
      "flights_count": 1,
      "id": 1,
      "in_space": true,
      "name": "Ava Chen",
      "nationality": [
        {}
      ],
      "status": {
        "name": "Ava Chen"
      },
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `agency.name` | string |  |
| `date_of_birth` | date |  |
| `flights_count` | number |  |
| `id` | number |  |
| `in_space` | boolean |  |
| `name` | string |  |
| `nationality` | array<object> |  |
| `status.name` | string |  |
| `type.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET astronauts/{{id}}/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-astronaut.md) for the provider-specific parameters and requirements.

