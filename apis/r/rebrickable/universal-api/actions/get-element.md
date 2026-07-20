# Rebrickable: Get Element

Retrieves a LEGO element from Rebrickable by element ID.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-element?connectionId=$CONNECTION_ID&elementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "elementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-element?${params}`, {
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
| `elementId` | string | yes | LEGO element ID to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {},
      "element_img_url": "https://example.com",
      "part": {},
      "part_img_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `element_img_url` | string |  |
| `part` | object |  |
| `part_img_url` | string |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/elements/:element_id/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-element.md) for the provider-specific parameters and requirements.

