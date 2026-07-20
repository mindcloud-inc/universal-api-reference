# Hunter: Get Leads List



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-leads-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-leads-list?connectionId=$CONNECTION_ID&leadsListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadsListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-leads-list?${params}`, {
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
| `leadsListId` | string | yes | Identifier of the leads list. |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "leads": [
        {}
      ],
      "leadsCount": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `leads` | array<object> |  |
| `leadsCount` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /leads_lists/:leadsListId` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leads-list.md) for the provider-specific parameters and requirements.

