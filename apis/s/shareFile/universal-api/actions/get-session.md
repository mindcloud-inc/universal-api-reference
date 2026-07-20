# ShareFile: Get Session



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session?${params}`, {
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
      "AuthenticationType": "string",
      "Id": "string",
      "IsAuthenticated": true,
      "OAuth2ClientName": "Ava Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "Principal": {},
      "Tool": "string",
      "url": "https://example.com",
      "Version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AuthenticationType` | string | The authentication type used for the session. |
| `Id` | string | The ShareFile session identifier. |
| `IsAuthenticated` | boolean | Whether the current session is authenticated. |
| `OAuth2ClientName` | string | The connected OAuth client name. |
| `odata.metadata` | string | The OData metadata URL for the session resource. |
| `odata.type` | string | The OData type name for the session resource. |
| `Principal` | object | The authenticated ShareFile principal details for the current session. |
| `Tool` | string | The ShareFile tool identifier for the session. |
| `url` | string | The API URL for the current session resource. |
| `Version` | string | The ShareFile session version field. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Sessions` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

