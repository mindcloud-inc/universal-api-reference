# Video Indexer (V2): Get Account

Retrieves an account from Video Indexer (V2).

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account?connectionId=$CONNECTION_ID&location=string&accountId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string",
  "accountId": "string",
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-account?${params}`, {
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
| `accessToken` | string | yes | An account access token with read permissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": {},
      "accountType": "string",
      "cName": "Ava Chen",
      "createTime": "string",
      "description": "string",
      "id": "string",
      "isPaid": true,
      "limitedAccessFeatures": {
        "isCelebrityRecognitionEnabled": true,
        "isFaceIdentificationEnabled": true
      },
      "location": "string",
      "moveToArmStartedDate": "string",
      "name": "Ava Chen",
      "owners": [
        {
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "provider": "string"
        }
      ],
      "state": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | object |  |
| `accountType` | string |  |
| `cName` | string |  |
| `createTime` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isPaid` | boolean |  |
| `limitedAccessFeatures.isCelebrityRecognitionEnabled` | boolean |  |
| `limitedAccessFeatures.isFaceIdentificationEnabled` | boolean |  |
| `location` | string |  |
| `moveToArmStartedDate` | string |  |
| `name` | string |  |
| `owners[].email` | string |  |
| `owners[].id` | string |  |
| `owners[].name` | string |  |
| `owners[].provider` | string |  |
| `state` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `GET /:location/Accounts/:accountId` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

