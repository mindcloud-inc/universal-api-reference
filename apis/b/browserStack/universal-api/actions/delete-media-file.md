# BrowserStack: Delete Media File

Deletes a media file from BrowserStack Automate.

```
DELETE https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/delete-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/delete-media-file?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/delete-media-file?${params}`, {
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
| `mediaId` | string | yes | BrowserStack media ID from List Uploaded Media Files. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BrowserStack API returns.

## Native endpoint

Through the native BrowserStack API, this operation is `DELETE https://api-cloud.browserstack.com/automate/custom_media/delete/:media_id` (base URL `https://api.browserstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-media-file.md) for the provider-specific parameters and requirements.

