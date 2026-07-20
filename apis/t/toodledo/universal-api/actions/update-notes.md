# Toodledo: Update Notes

Updates existing notes in Toodledo.

```
PUT https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | yes | JSON-encoded array of up to 50 note objects. Each object must include an id. |

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

Through the native Toodledo API, this operation is `POST /notes/edit.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notes.md) for the provider-specific parameters and requirements.

