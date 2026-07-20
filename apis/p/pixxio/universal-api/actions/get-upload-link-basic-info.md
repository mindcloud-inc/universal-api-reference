# pixx.io: Get Upload Link Basic Info

Retrieves basic upload link info from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-upload-link-basic-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-upload-link-basic-info?connectionId=$CONNECTION_ID&shareKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shareKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-upload-link-basic-info?${params}`, {
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
| `shareKey` | string | yes | The upload link share key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "uploadLink": {
        "id": 1,
        "name": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `uploadLink` | object |  |
| `uploadLink.id` | number |  |
| `uploadLink.name` | string |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /uploadLinks/basicInfo` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-link-basic-info.md) for the provider-specific parameters and requirements.

