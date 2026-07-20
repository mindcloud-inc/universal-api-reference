# retailCRM: List Payment Types

Retrieves payment types from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-payment-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-payment-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-payment-types?${params}`, {
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
      "deliveryTypes": [
        "string"
      ],
      "name": "Ava Chen",
      "paymentStatuses": [
        "string"
      ],
      "sites": [
        "string"
      ]
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
| `deliveryTypes[]` | string |  |
| `name` | string |  |
| `paymentStatuses[]` | string |  |
| `sites` | array |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /reference/payment-types` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-types.md) for the provider-specific parameters and requirements.

