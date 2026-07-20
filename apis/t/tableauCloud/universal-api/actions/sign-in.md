# Tableau Cloud: Sign In

Signs in to Tableau Cloud and returns an auth token.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/sign-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/sign-in?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/sign-in?${params}`, {
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
      "estimatedTimeToExpiration": "string",
      "site": {
        "contentUrl": "https://example.com",
        "id": "string"
      },
      "token": "string",
      "user": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimatedTimeToExpiration` | string | Approximate PAT time to expiration. |
| `site.contentUrl` | string | Signed-in site content URL. |
| `site.id` | string | Signed-in site ID. |
| `token` | string | Tableau authentication token. |
| `user.id` | string | Signed-in user ID. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `POST /auth/signin` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-in.md) for the provider-specific parameters and requirements.

