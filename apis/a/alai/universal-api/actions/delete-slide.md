# Alai: Delete Slide

Permanently deletes a slide from an Alai presentation.

```
DELETE https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-slide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-slide?connectionId=$CONNECTION_ID&presentationId=string&slideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string",
  "slideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alai/latest/actions/delete-slide?${params}`, {
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
| `presentationId` | string | yes | Target presentation identifier. |
| `slideId` | string | yes | Slide identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Alai API, this operation is `DELETE /presentations/:presentation_id/slides/:slide_id` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-slide.md) for the provider-specific parameters and requirements.

