# CDC Content Services: Get Media Embed Code

Retrieves media embed code from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-embed-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDC Content Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-embed-code?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-embed-code?${params}`, {
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
| `mediaId` | number | yes | CDC media identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | CDC embed code string returned as the top-level results value. |

## Native endpoint

Through the native CDC Content Services API, this operation is `GET /v2/resources/media/[:mediaId]/embed` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-embed-code.md) for the provider-specific parameters and requirements.

