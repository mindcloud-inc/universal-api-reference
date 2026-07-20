# VoilaNorbert: Get List

Retrieves one list from VoilaNorbert.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-list?${params}`, {
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
| `id` | number | yes | The list id to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": 1,
      "created": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | number |  |
| `created` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /lists/:id` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

