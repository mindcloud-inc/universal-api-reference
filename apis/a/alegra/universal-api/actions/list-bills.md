# Alegra: List Bills

Retrieves purchase bills from your Alegra account.

```
GET https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-bills?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-bills?${params}`, {
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
| `metadata` | boolean | no |  |
| `start` | number | no |  |
| `limit` | number | no |  |
| `orderDirection` | string | no |  |
| `orderField` | string | no |  |
| `billNumber` | string | no |  |
| `clientName` | string | no |  |
| `date` | string | no |  |
| `dueDate` | string | no |  |
| `status` | string | no |  |
| `itemId` | number | no |  |
| `clientId` | number | no |  |
| `providerName` | string | no |  |
| `uuid` | string | no |  |
| `purchaseorderId` | number | no |  |
| `type` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `GET /bills` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

