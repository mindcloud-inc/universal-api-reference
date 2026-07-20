# Centers for Disease Control and Prevention: Get Media Content

Retrieves media content from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-content?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-content?${params}`, {
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
| `mediaId` | number | yes | The identifier of the media. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | string | Syndicated content returned by the CDC API. |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/media/:mediaId/content` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-content.md) for the provider-specific parameters and requirements.

