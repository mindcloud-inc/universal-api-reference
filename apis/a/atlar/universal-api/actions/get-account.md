# Atlar: Get account

Retrieves an account from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-account?${params}`, {
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
      "currency": "string",
      "entityId": "string",
      "etag": "string",
      "externalId": "string",
      "fictive": true,
      "id": "string",
      "identifiers": [
        {}
      ],
      "market": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organizationId": "string",
      "paymentOptions": {},
      "routing": [
        {}
      ],
      "status": "string",
      "thirdPartyId": "string",
      "type": "string",
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
| `currency` | string |  |
| `entityId` | string |  |
| `etag` | string |  |
| `externalId` | string |  |
| `fictive` | boolean |  |
| `id` | string |  |
| `identifiers` | array<object> |  |
| `market` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `paymentOptions` | object |  |
| `routing` | array<object> |  |
| `status` | string |  |
| `thirdPartyId` | string |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2/accounts/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

