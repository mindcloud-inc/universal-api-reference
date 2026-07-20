# Google Slides: Delete Presentation

Deletes an existing presentation file from Google Slides.

```
DELETE https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-presentation?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-presentation?${params}`, {
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
| `fileId` | string | yes | The ID of the presentation file to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Slides API returns.

## Native endpoint

Through the native Google Slides API, this operation is `DELETE https://www.googleapis.com/drive/v3/files/:fileId` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-presentation.md) for the provider-specific parameters and requirements.

