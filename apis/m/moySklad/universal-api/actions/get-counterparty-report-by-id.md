# MoySklad: Get counterparty report by ID

Retrieves the counterparty report from MoySklad by ID.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-counterparty-report-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-counterparty-report-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-counterparty-report-by-id?${params}`, {
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
| `id` | string | yes | MoySklad counterparty ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "profit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `id` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `profit` | number |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET report/counterparty/:id` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-counterparty-report-by-id.md) for the provider-specific parameters and requirements.

