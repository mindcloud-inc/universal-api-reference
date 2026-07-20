# retailCRM: List Stores

Retrieves stores from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-stores?${params}`, {
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
      "address": {
        "countryIso": "string"
      },
      "code": "string",
      "inventoryType": "string",
      "name": "Ava Chen",
      "ordering": "string",
      "type": "string",
      "workTime": {
        "fr": [
          "string"
        ],
        "mo": [
          "string"
        ],
        "sa": [
          "string"
        ],
        "su": [
          "string"
        ],
        "th": [
          "string"
        ],
        "tu": [
          "string"
        ],
        "we": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address.countryIso` | string |  |
| `code` | string |  |
| `inventoryType` | string |  |
| `name` | string |  |
| `ordering` | string |  |
| `type` | string |  |
| `workTime.fr` | array |  |
| `workTime.mo` | array |  |
| `workTime.sa` | array |  |
| `workTime.su` | array |  |
| `workTime.th` | array |  |
| `workTime.tu` | array |  |
| `workTime.we` | array |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /reference/stores` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores.md) for the provider-specific parameters and requirements.

