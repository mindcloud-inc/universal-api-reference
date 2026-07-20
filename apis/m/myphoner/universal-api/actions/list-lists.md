# Myphoner: List Lists

Retrieves all existing lists from Myphoner.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-lists?${params}`, {
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
| `lockedOnDefaults` | boolean | no | Return only lists that guarantee Myphoner default fields are defined. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "leadsCount": 1,
      "location": "string",
      "lockedOnDefaults": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `leadsCount` | number |  |
| `location` | string |  |
| `lockedOnDefaults` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /lists` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

