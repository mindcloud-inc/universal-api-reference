# Dwolla: Get Funding Source Balance

Retrieves balance details for a funding source in Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source-balance?${params}`, {
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
| `id` | string | no | Dwolla funding source ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "balance": {},
      "lastUpdated": "string",
      "total": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for the funding-source balance resource. |
| `balance` | object | Available balance for the funding source. |
| `lastUpdated` | string | Timestamp of the most recent balance update. |
| `total` | object | Total balance for the funding source. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /funding-sources/[:id]/balance` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-funding-source-balance.md) for the provider-specific parameters and requirements.

