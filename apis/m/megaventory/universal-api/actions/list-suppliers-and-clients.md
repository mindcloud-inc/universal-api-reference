# Megaventory: List Suppliers and Clients

Retrieves supplier and client records from Megaventory.

```
GET https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-suppliers-and-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-suppliers-and-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-suppliers-and-clients?${params}`, {
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
| `Filters` | list<object> | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | number | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | boolean | no | Include archived supplier or client records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mvSupplierClients": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mvSupplierClients` | array<object> |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/SupplierClientGet` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers-and-clients.md) for the provider-specific parameters and requirements.

