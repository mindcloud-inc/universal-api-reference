# Toodledo: List Outlines

Retrieves outlines from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-outlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-outlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-outlines?${params}`, {
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
| `before` | number | no | Return only outlines modified before this GMT Unix timestamp. |
| `after` | number | no | Return only outlines modified after this GMT Unix timestamp. |
| `id` | string | no | Fetch a single outline by its hexadecimal Toodledo outline ID. |
| `start` | number | no | Number of records to skip before returning results. |
| `num` | number | no | Maximum number of outlines to return. Toodledo documents a default and max of 1000. |

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

Through the native Toodledo API, this operation is `GET /outlines/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-outlines.md) for the provider-specific parameters and requirements.

