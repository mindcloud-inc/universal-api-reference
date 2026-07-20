# Video Indexer (V2): Get Account Access Token

Retrieves an account access token from Video Indexer (V2).

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account-access-token?connectionId=$CONNECTION_ID&location=string&accountId=string&allowEdit=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string",
  "accountId": "string",
  "allowEdit": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account-access-token?${params}`, {
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
| `location` | string | yes | Azure region to route the call to, such as Trial for trial accounts. |
| `accountId` | string | yes | Video Indexer account ID. |
| `allowEdit` | boolean | yes | Whether the returned account access token can be used for write operations. Default: `false`. |

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

Through the native Video Indexer (V2) API, this operation is `GET /Auth/:location/Accounts/:accountId/AccessToken` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-access-token.md) for the provider-specific parameters and requirements.

