# Emelia: List Credentials

Retrieves scraper credentials from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-credentials?${params}`, {
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
      "data": {
        "scrapAuthes": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "name": {},
            "status": "string",
            "token": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.scrapAuthes[].createdAt` | date |  |
| `data.scrapAuthes[].name` | object |  |
| `data.scrapAuthes[].status` | string |  |
| `data.scrapAuthes[].token` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

