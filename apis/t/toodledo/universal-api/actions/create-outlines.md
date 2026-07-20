# Toodledo: Create Outlines

Creates outlines in Toodledo.

```
POST https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-outlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-outlines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outlines": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-outlines', {
  method: 'POST',
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
| `outlines` | string | yes | JSON-encoded array of up to 50 outline objects. Each outline must include title and ref. |

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
      "ref": "string",
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
| `ref` | string | Client correlation reference. |
| `title` | string | Outline title. |
| `version` | number | Outline version number. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /outlines/add.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-outlines.md) for the provider-specific parameters and requirements.

