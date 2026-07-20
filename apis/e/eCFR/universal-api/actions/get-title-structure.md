# eCFR: Get Title Structure

Retrieves a title structure from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-title-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-title-structure?connectionId=$CONNECTION_ID&date=string&title=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "title": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-title-structure?${params}`, {
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
| `date` | string | yes | eCFR version date in YYYY-MM-DD format. |
| `title` | number | yes | CFR title number, such as 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "identifier": "string",
      "label": "string",
      "label_description": "string",
      "label_level": "string",
      "reserved": true,
      "size": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> | Child hierarchy nodes. |
| `identifier` | string | CFR hierarchy identifier. |
| `label` | string | Display label for the hierarchy node. |
| `label_description` | string | Description for the hierarchy node. |
| `label_level` | string | Label level for the hierarchy node. |
| `reserved` | boolean | Whether this hierarchy node is reserved. |
| `size` | number | Approximate content size. |
| `type` | string | Hierarchy node type. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/versioner/v1/structure/:date/title-:title.json` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-title-structure.md) for the provider-specific parameters and requirements.

