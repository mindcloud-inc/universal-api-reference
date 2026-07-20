# Magileads: List PRM Contacts

Retrieves your PRM contacts from Magileads.

```
GET https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-contacts?${params}`, {
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
      "current_page": "string",
      "next_page": "string",
      "number_of_pages": 1,
      "number_of_results": 1,
      "previous_page": "string",
      "results": [
        {}
      ],
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | string |  |
| `next_page` | string |  |
| `number_of_pages` | number |  |
| `number_of_results` | number |  |
| `previous_page` | string |  |
| `results` | array<object> |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `GET /prm/contacts` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prm-contacts.md) for the provider-specific parameters and requirements.

