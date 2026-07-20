# Synchroteam: List Sites by Customer ID

Retrieves sites from Synchroteam for a specific customer ID.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-sites-by-customer-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-sites-by-customer-id?connectionId=$CONNECTION_ID&paramValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-sites-by-customer-id?${params}`, {
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
| `paramValue` | string | yes | Customer id to list sites for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "customer": {
        "id": 1,
        "myId": "string",
        "name": "Ava Chen"
      },
      "id": 1,
      "myId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `customer.id` | number |  |
| `customer.myId` | string |  |
| `customer.name` | string |  |
| `id` | number |  |
| `myId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Site/List/byCustomer/id/:paramValue` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites-by-customer-id.md) for the provider-specific parameters and requirements.

