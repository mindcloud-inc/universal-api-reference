# Trolley: List Offline Payments

Retrieves all offline payments from Trolley.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-offline-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-offline-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-offline-payments?${params}`, {
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
| `page` | string | no | Page number |
| `pageSize` | string | no | Page size |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "offlinePayments": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `offlinePayments` | array<object> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `GET /v1/offline-payments` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offline-payments.md) for the provider-specific parameters and requirements.

