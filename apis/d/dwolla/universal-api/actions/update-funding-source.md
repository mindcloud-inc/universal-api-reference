# Dwolla: Update Funding Source

Updates a bank funding source in Dwolla.

```
PUT https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-funding-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-funding-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-funding-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Dwolla funding source ID. |
| `name` | string | yes | Updated funding source display name |
| `routingNumber` | string | no | Updated bank routing number |
| `accountNumber` | string | no | Updated bank account number |
| `bankAccountType` | string | no | Updated bank account type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "bankAccountType": "string",
      "channels": [
        "string"
      ],
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "removed": true,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for the funding source. |
| `bankAccountType` | string | Bank-account subtype for the funding source. |
| `channels` | array<string> | Transfer channels available for the funding source. |
| `created` | string | Funding-source creation timestamp. |
| `id` | string | Dwolla funding source identifier. |
| `name` | string | Funding-source display name. |
| `removed` | boolean | Whether the funding source has been removed. |
| `status` | string | Current Dwolla funding-source status. |
| `type` | string | Funding-source type. |

## Native endpoint

Through the native Dwolla API, this operation is `POST /funding-sources/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-funding-source.md) for the provider-specific parameters and requirements.

