# NobelSMS: List Blacklist Entries

Retrieves blacklist entries from NobelSMS.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-blacklist-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-blacklist-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-blacklist-entries?${params}`, {
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
| `bnumber` | number | no | B-number. |
| `tagIds` | string | no | Comma-separated list of tag IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bnumber": "string",
      "id": 1,
      "tag_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bnumber` | string |  |
| `id` | number |  |
| `tag_id` | number |  |

## Native endpoint

Through the native NobelSMS API, this operation is `GET /black_list` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-blacklist-entries.md) for the provider-specific parameters and requirements.

