# Dwolla: Get Transfer

Retrieves details for a transfer from Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-transfer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-transfer?${params}`, {
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
| `id` | string | no | Dwolla transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "amount": {},
      "clearing": {},
      "created": "string",
      "id": "string",
      "individualAchId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related transfer resources. |
| `amount` | object | Transfer amount and currency. |
| `clearing` | object | Transfer clearing metadata. |
| `created` | string | Transfer creation timestamp. |
| `id` | string | Dwolla transfer identifier. |
| `individualAchId` | string | ACH identifier for the transfer when available. |
| `status` | string | Current Dwolla transfer status. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /transfers/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transfer.md) for the provider-specific parameters and requirements.

