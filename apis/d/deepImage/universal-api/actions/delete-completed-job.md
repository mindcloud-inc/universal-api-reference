# DeepImage: Delete Completed Job

Deletes a completed processing job from DeepImage.

```
DELETE https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/delete-completed-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/delete-completed-job?connectionId=$CONNECTION_ID&hash=a8784c00-dc6b-11ee-ad50-9ec3ba0205c0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "a8784c00-dc6b-11ee-ad50-9ec3ba0205c0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/delete-completed-job?${params}`, {
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
| `hash` | string | yes | The completed processing job hash to delete from DeepImage. Example: `a8784c00-dc6b-11ee-ad50-9ec3ba0205c0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message returned after DeepImage removes job images. |

## Native endpoint

Through the native DeepImage API, this operation is `DELETE /rest_api/result/:hash` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-completed-job.md) for the provider-specific parameters and requirements.

