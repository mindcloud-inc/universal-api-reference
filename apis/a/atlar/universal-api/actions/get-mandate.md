# Atlar: Get mandate

Retrieves a mandate from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-mandate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-mandate?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-mandate?${params}`, {
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
      "connectionInstructionId": "string",
      "counterpartyId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creditorReference": "string",
      "destinationAccountId": "string",
      "etag": "string",
      "externalAccountId": "string",
      "externalId": "string",
      "id": "string",
      "mandateReference": "string",
      "metadata": {},
      "organizationId": "string",
      "scheme": "string",
      "signatureDate": "2026-05-07T12:00:00.000Z",
      "source": {},
      "sourceHolder": {},
      "status": "string",
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
| `connectionInstructionId` | string |  |
| `counterpartyId` | string |  |
| `created` | date |  |
| `creditorReference` | string |  |
| `destinationAccountId` | string |  |
| `etag` | string |  |
| `externalAccountId` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `mandateReference` | string |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `scheme` | string |  |
| `signatureDate` | date |  |
| `source` | object |  |
| `sourceHolder` | object |  |
| `status` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /payments/v2/mandates/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mandate.md) for the provider-specific parameters and requirements.

