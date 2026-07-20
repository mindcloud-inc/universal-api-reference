# Tako: Export Knowledge Card to PowerPoint

Exports a Tako knowledge card to PowerPoint.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/export-knowledge-card-to-power-point
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/export-knowledge-card-to-power-point?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/export-knowledge-card-to-power-point?${params}`, {
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
| `cardId` | string | yes | ID of the knowledge card to export as a PowerPoint deck. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | PowerPoint slide deck file download response |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/powerpoint` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-knowledge-card-to-power-point.md) for the provider-specific parameters and requirements.

