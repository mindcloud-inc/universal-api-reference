# Toodledo: Update Lists

Updates existing lists in Toodledo.

```
PUT https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lists": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-lists', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lists": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lists` | string | yes | JSON-encoded array of up to 50 list objects. Each list must include id and version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "cols": [
        {}
      ],
      "id": "string",
      "keywords": "string",
      "modified": 1,
      "note": "string",
      "rows": 1,
      "title": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number | Creation timestamp. |
| `cols` | array<object> | Column definitions. |
| `id` | string | List ID. |
| `keywords` | string | List keywords. |
| `modified` | number | Last modification timestamp. |
| `note` | string | List note. |
| `rows` | number | Number of rows. |
| `title` | string | List title. |
| `version` | number | List version number. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /lists/edit.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lists.md) for the provider-specific parameters and requirements.

