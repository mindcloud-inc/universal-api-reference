# BaseLinker: Get Order Statuses

Retrieves order statuses from BaseLinker.

```
GET https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "statuses": [
        {
          "color": "string",
          "id": 1,
          "name": "Ava Chen",
          "nameForCustomer": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `statuses[].color` | string |  |
| `statuses[].id` | number |  |
| `statuses[].name` | string |  |
| `statuses[].nameForCustomer` | string |  |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-statuses.md) for the provider-specific parameters and requirements.

