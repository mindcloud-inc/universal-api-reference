# EasyContent: Check API Key

Checks an EasyContent API key and returns its project.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key?${params}`, {
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
      "projectId": 1,
      "projectTitle": "string",
      "projectUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectId` | number |  |
| `projectTitle` | string |  |
| `projectUrl` | string |  |

## Native endpoint

Through the native EasyContent API, this operation is `GET /v2/content/auth` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-api-key.md) for the provider-specific parameters and requirements.

