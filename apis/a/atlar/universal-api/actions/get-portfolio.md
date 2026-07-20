# Atlar: Get portfolio

Retrieves a portfolio from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-portfolio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-portfolio?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-portfolio?${params}`, {
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
| `id` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliationId": "string",
      "alias": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "entityId": "string",
      "etag": "string",
      "id": "string",
      "identifiers": [
        {}
      ],
      "metadata": {},
      "organizationId": "string",
      "thirdPartyId": "string",
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
| `affiliationId` | string |  |
| `alias` | string |  |
| `created` | date |  |
| `entityId` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `identifiers` | array<object> |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `thirdPartyId` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2beta/portfolios/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portfolio.md) for the provider-specific parameters and requirements.

