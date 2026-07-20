# ArcSite: Get Drawing Payment

Retrieves payment details for one ArcSite drawing.

```
GET https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing-payment?connectionId=$CONNECTION_ID&drawingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "drawingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing-payment?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "deposit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deposit` | number |  |

## Native endpoint

Through the native ArcSite API, this operation is `GET /drawings/:drawingId/payment` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drawing-payment.md) for the provider-specific parameters and requirements.

