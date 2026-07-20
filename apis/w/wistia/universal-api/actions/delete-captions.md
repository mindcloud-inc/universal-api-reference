# Wistia: Delete Captions

Deletes captions for a Wistia media language.

```
DELETE https://connect.mindcloud.co/v1/universal/wistia/latest/actions/delete-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/delete-captions?connectionId=$CONNECTION_ID&mediaHashedId=string&languageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaHashedId": "string",
  "languageCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/delete-captions?${params}`, {
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
| `mediaHashedId` | string | yes |  |
| `languageCode` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wistia API returns.

## Native endpoint

Through the native Wistia API, this operation is `DELETE /modern/medias/:mediaHashedId/captions/:languageCode` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-captions.md) for the provider-specific parameters and requirements.

