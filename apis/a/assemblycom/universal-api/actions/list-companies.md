# Assembly.com: List Companies

Retrieves companies from Assembly.com.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-companies?${params}`, {
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
| `name` | string | no | The name of the company to query for. |
| `isPlaceholder` | boolean | no | If true, filter for all placeholder companies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fallbackColor": "string",
          "iconImageUrl": "https://example.com",
          "id": "string",
          "isPlaceholder": true,
          "name": "Ava Chen",
          "object": "string"
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
| `data[].createdAt` | date |  |
| `data[].fallbackColor` | string |  |
| `data[].iconImageUrl` | string |  |
| `data[].id` | string |  |
| `data[].isPlaceholder` | boolean |  |
| `data[].name` | string |  |
| `data[].object` | string |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /companies` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

