# Atlar: Get external account

Retrieves an external account from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-external-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-external-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-external-account?${params}`, {
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
      "alias": "string",
      "counterpartyId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "entityIds": [
        {}
      ],
      "etag": "string",
      "externalId": "string",
      "id": "string",
      "identifiers": [
        {}
      ],
      "market": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organizationId": "string",
      "routing": [
        {}
      ],
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
| `alias` | string |  |
| `counterpartyId` | string |  |
| `created` | date |  |
| `entityIds` | array<object> |  |
| `etag` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `identifiers` | array<object> |  |
| `market` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `routing` | array<object> |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /payments/v2/external-accounts/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-external-account.md) for the provider-specific parameters and requirements.

