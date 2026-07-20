# TelTel: List Contact Group Contacts

Retrieves contacts from a TelTel contact group.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-contact-group-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-contact-group-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-contact-group-contacts?${params}`, {
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
      "groupId": "string",
      "id": 1,
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `id` | number |  |
| `phone` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /contacts/groups/{id}/contacts` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-group-contacts.md) for the provider-specific parameters and requirements.

