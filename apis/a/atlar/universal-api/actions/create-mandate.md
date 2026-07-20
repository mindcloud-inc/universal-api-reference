# Atlar: Create mandate

Creates a mandate in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-mandate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-mandate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheme": "string",
  "externalAccountId": "string",
  "creditorReference": "string",
  "mandateReference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-mandate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scheme": "string",
    "externalAccountId": "string",
    "creditorReference": "string",
    "mandateReference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheme` | string<string> | yes |  |
| `externalAccountId` | string<string> | yes |  |
| `creditorReference` | string<string> | yes |  |
| `mandateReference` | string<string> | yes |  |

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

Through the native Atlar API, this operation is `POST /payments/v2/mandates` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mandate.md) for the provider-specific parameters and requirements.

