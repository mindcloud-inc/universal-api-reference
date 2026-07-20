# Alai: Delete Presentation

Permanently deletes a presentation from Alai.

```
DELETE https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-presentation?connectionId=$CONNECTION_ID&presentationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-presentation?${params}`, {
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
| `presentationId` | string | yes | Presentation identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "presentationId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presentationId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Alai API, this operation is `DELETE /presentations/:presentation_id` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-presentation.md) for the provider-specific parameters and requirements.

