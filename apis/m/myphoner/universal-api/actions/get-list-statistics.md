# Myphoner: Get List Statistics

Retrieves lead statistics for a list in Myphoner.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-list-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-list-statistics?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-list-statistics?${params}`, {
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
| `listId` | number | yes | The Myphoner list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "leadsCount": 1,
      "leadsCounts": {},
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
| `leadsCounts` | object |  |
| `location` | string |  |
| `lockedOnDefaults` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /lists/:listId/stats` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-statistics.md) for the provider-specific parameters and requirements.

