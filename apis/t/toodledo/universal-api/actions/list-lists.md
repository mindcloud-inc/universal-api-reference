# Toodledo: List Lists

Retrieves lists from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-lists?${params}`, {
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
| `before` | number | no | Return only lists modified before this GMT Unix timestamp. |
| `after` | number | no | Return only lists modified after this GMT Unix timestamp. |
| `id` | string | no | Fetch a single list by its hexadecimal Toodledo list ID. |
| `start` | number | no | Number of records to skip before returning results. |
| `num` | number | no | Maximum number of lists to return. Toodledo documents a default and max of 1000. |

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

Through the native Toodledo API, this operation is `GET /lists/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

