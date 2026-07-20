# Autype: Get API Key Info



```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info?${params}`, {
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
      "createdByUserId": "string",
      "creditsAvailable": 1,
      "orgId": "string",
      "orgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByUserId` | string |  |
| `creditsAvailable` | number |  |
| `orgId` | string |  |
| `orgName` | string |  |

## Native endpoint

Through the native Autype API, this operation is `GET /api-key/info` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-info.md) for the provider-specific parameters and requirements.

