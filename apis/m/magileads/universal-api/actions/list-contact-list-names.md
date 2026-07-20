# Magileads: List Contact List Names

Retrieves contact list IDs and names from Magileads.

```
GET https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-names?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-names?${params}`, {
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
      "contact_lists": [
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
| `contact_lists` | array<object> |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `GET /contact-lists/names` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-list-names.md) for the provider-specific parameters and requirements.

