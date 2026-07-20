# VoilaNorbert: List Contacts

Retrieves a list of contacts from VoilaNorbert.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-contacts?${params}`, {
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
      "has_next": true,
      "has_prev": true,
      "page": 1,
      "pages": 1,
      "result": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_next` | boolean |  |
| `has_prev` | boolean |  |
| `page` | number |  |
| `pages` | number |  |
| `result` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /contacts/` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

