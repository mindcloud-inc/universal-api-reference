# Microsoft Exchange: Authorize Application



```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application?${params}`, {
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
      "expiresIn": 1,
      "extExpiresIn": 1,
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `expiresIn` | number |  |
| `extExpiresIn` | number |  |
| `tokenType` | string |  |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `POST https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize-application.md) for the provider-specific parameters and requirements.

