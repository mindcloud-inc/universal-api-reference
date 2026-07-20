# Lob: Retrieve Bank Account



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-bank-account?connectionId=$CONNECTION_ID&bankId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bankId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/retrieve-bank-account?${params}`, {
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
| `bankId` | string | yes | Bank account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_number": "string",
      "account_type": "string",
      "bank_name": "Ava Chen",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "id": "string",
      "metadata": {},
      "object": "string",
      "routing_number": "string",
      "signatory": "string",
      "signature_url": "https://example.com",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | string |  |
| `account_type` | string |  |
| `bank_name` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `routing_number` | string |  |
| `signatory` | string |  |
| `signature_url` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `GET /bank_accounts/:bank_id` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bank-account.md) for the provider-specific parameters and requirements.

