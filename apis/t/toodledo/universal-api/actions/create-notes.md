# Toodledo: Create Notes

Creates notes in Toodledo.

```
POST https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-notes', {
  method: 'POST',
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
| `notes` | string | yes | JSON-encoded array of up to 50 note objects using title, folder, private, added, text, and optional ref. |

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
      "ref": "string",
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
| `ref` | string | Client correlation reference. |
| `text` | string | Note body. |
| `title` | string | Note title. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /notes/add.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-notes.md) for the provider-specific parameters and requirements.

