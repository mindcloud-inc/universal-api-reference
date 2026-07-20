# Salescamp: Get Deal



```
GET https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salescamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/get-deal?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/get-deal?${params}`, {
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
| `itemId` | string | yes | Resource ID of the deal |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Salescamp API, this operation is `GET /v1/collections/69cd24c3f24a3ccfd974bb19/items/:itemId` (base URL `https://api.salescamp.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

