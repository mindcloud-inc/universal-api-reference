# Clio Grow: List Inbox Leads



```
GET https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-inbox-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-inbox-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-inbox-leads?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdSince` | date | no | Only include inbox leads created on or after this ISO-8601 timestamp. |
| `updatedSince` | date | no | Only include inbox leads updated on or after this ISO-8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fromMessage": "string",
      "fromSource": "string",
      "id": 1,
      "lastName": "Chen",
      "phoneNumber": "string",
      "referringUrl": "https://example.com",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fromMessage` | string |  |
| `fromSource` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `referringUrl` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `GET /inbox_leads` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbox-leads.md) for the provider-specific parameters and requirements.

