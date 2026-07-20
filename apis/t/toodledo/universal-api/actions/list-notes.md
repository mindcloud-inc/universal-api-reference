# Toodledo: List Notes

Retrieves notes from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-notes?${params}`, {
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
| `before` | number | no | Return only notes modified before this GMT Unix timestamp. |
| `after` | number | no | Return only notes modified after this GMT Unix timestamp. |
| `id` | number | no | Fetch a single note by its numeric Toodledo note ID. |
| `start` | number | no | Number of records to skip before returning results. |
| `num` | number | no | Maximum number of notes to return. Toodledo documents a default and max of 1000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "folder": 1,
      "id": 1,
      "modified": 1,
      "private": 1,
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number | Creation timestamp. |
| `folder` | number | Folder ID. |
| `id` | number | Note ID. |
| `modified` | number | Last modification timestamp. |
| `private` | number | Private flag. |
| `text` | string | Note body. |
| `title` | string | Note title. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /notes/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

