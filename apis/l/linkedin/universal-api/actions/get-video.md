# LinkedIn: Get Video

Retrieves a video from LinkedIn.

```
GET https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-video?connectionId=$CONNECTION_ID&videoUrn=urn%253Ali%253Avideo%253AD4D10AQGWLEc0FUTwqw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoUrn": "urn%3Ali%3Avideo%3AD4D10AQGWLEc0FUTwqw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-video?${params}`, {
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
| `videoUrn` | string | yes | Video URN, for example urn:li:video:{id}. Example: `urn%3Ali%3Avideo%3AD4D10AQGWLEc0FUTwqw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "owner": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `owner` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LinkedIn API, this operation is `GET /rest/videos/:videoUrn` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

