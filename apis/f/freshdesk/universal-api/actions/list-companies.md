# Freshdesk: List Companies

Retrieves a list of companies from Freshdesk.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-companies?${params}`, {
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
| `updatedSince` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTier": "string",
      "createdAt": "string",
      "description": "string",
      "domains": [
        "string"
      ],
      "id": 1,
      "industry": "string",
      "name": "Ava Chen",
      "note": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTier` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `domains` | array<string> |  |
| `id` | number |  |
| `industry` | string |  |
| `name` | string |  |
| `note` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `GET /companies` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

