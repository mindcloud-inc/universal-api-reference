# ArcSite: Get Takeoff Line Items

Retrieves takeoff line items from an ArcSite drawing.

```
GET https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-takeoff-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-takeoff-line-items?connectionId=$CONNECTION_ID&drawingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "drawingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-takeoff-line-items?${params}`, {
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
| `drawingId` | string | yes | The ID of the drawing. |
| `drawingVersionId` | string | no | The ID of the drawing version. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ArcSite API returns.

## Native endpoint

Through the native ArcSite API, this operation is `GET /drawings/:drawingId/takeoff_items` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-takeoff-line-items.md) for the provider-specific parameters and requirements.

