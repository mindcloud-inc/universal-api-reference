# Video Indexer (V2): Get Video ID By External ID

Retrieves a video ID from an external ID in Video Indexer (V2).

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-id-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-id-by-external-id?connectionId=$CONNECTION_ID&location=string&accountId=string&externalId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string",
  "accountId": "string",
  "externalId": "string",
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-id-by-external-id?${params}`, {
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
| `location` | string | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | string | yes | Video Indexer account ID. |
| `externalId` | string | yes | The external ID. |
| `accessToken` | string | yes | An account access token with read permissions. |

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
| `response` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `GET /:location/Accounts/:accountId/Videos/GetIdByExternalId` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-id-by-external-id.md) for the provider-specific parameters and requirements.

