# SeaTable: Get Base Token With API Token

Retrieves a SeaTable base token with an API token.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "appName": "Ava Chen",
      "dtableName": "Ava Chen",
      "dtableServer": "string",
      "dtableUuid": "string",
      "useApiGateway": true,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `appName` | string |  |
| `dtableName` | string |  |
| `dtableServer` | string |  |
| `dtableUuid` | string |  |
| `useApiGateway` | boolean |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api/v2.1/dtable/app-access-token/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-base-token-with-api-token.md) for the provider-specific parameters and requirements.

