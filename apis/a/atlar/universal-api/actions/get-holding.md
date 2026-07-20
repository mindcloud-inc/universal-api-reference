# Atlar: Get holding

Retrieves a holding from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding?connectionId=$CONNECTION_ID&pid=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding?${params}`, {
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
| `pid` | string<string> | yes |  |
| `id` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "etag": "string",
      "id": "string",
      "identifiers": [
        {}
      ],
      "market": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organizationId": "string",
      "portfolioId": "string",
      "position": {},
      "taxId": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `currency` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `identifiers` | array<object> |  |
| `market` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `portfolioId` | string |  |
| `position` | object |  |
| `taxId` | string |  |
| `type` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2beta/portfolios/{pid}/holdings/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-holding.md) for the provider-specific parameters and requirements.

