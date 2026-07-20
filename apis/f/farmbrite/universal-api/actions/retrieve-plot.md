# Farmbrite: Retrieve plot

Retrieves a specific plot from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-plot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-plot?connectionId=$CONNECTION_ID&plotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "plotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-plot?${params}`, {
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
| `plotId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "electronicId": "string",
      "estimatedValue": "string",
      "grazingRestDays": "string",
      "id": "string",
      "internalId": "string",
      "layoutType": "string",
      "lightProfile": "string",
      "size": "string",
      "status": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `electronicId` | string |  |
| `estimatedValue` | string |  |
| `grazingRestDays` | string |  |
| `id` | string |  |
| `internalId` | string |  |
| `layoutType` | string |  |
| `lightProfile` | string |  |
| `size` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /plots/:plot_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-plot.md) for the provider-specific parameters and requirements.

