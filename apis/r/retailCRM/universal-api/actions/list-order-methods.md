# retailCRM: List Order Methods

Retrieves order methods from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-order-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-order-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-order-methods?${params}`, {
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
      "active": true,
      "code": "string",
      "defaultForApi": true,
      "defaultForCrm": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `code` | string |  |
| `defaultForApi` | boolean |  |
| `defaultForCrm` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /reference/order-methods` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-methods.md) for the provider-specific parameters and requirements.

