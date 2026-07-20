# CheckFlow: Validate API Key



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/validate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/validate-api-key?${params}`, {
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
      "isValid": true,
      "teamId": 1,
      "teamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean | Whether the provided API key is valid. |
| `teamId` | number | The numeric team ID associated with the API key. |
| `teamName` | string | The team name associated with the API key. |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/authentication/validate` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-api-key.md) for the provider-specific parameters and requirements.

