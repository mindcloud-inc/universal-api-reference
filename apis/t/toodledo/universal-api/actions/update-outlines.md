# Toodledo: Update Outlines

Updates existing outlines in Toodledo.

```
PUT https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-outlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-outlines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outlines": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/update-outlines', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outlines": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outlines` | string | yes | JSON-encoded array of up to 50 outline objects. Each outline must include id and version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "hidden": true,
      "id": "string",
      "keywords": "string",
      "modified": 1,
      "note": "string",
      "outline": {},
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
| `hidden` | boolean | Hide checked nodes flag. |
| `id` | string | Outline ID. |
| `keywords` | string | Outline keywords. |
| `modified` | number | Last modification timestamp. |
| `note` | string | Outline note. |
| `outline` | object | Outline tree payload. |
| `title` | string | Outline title. |
| `version` | number | Outline version number. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /outlines/edit.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-outlines.md) for the provider-specific parameters and requirements.

