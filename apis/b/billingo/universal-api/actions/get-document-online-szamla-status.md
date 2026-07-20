# Billingo: Get Document Online Szamla Status

Retrieves a document Online Szamla status from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-online-szamla-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-online-szamla-status?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-online-szamla-status?${params}`, {
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
| `id` | number | yes | Billingo document ID from the path. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ],
      "status": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> |  |
| `status` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents/:id/online-szamla` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-online-szamla-status.md) for the provider-specific parameters and requirements.

