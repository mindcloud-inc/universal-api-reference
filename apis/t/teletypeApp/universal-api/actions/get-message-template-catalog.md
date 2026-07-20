# Teletype App: Get Message Template Catalog

Retrieves the message template catalog from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-message-template-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-message-template-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-message-template-catalog?${params}`, {
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
      "directories": [
        {}
      ],
      "withoutDirectories": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directories` | array<object> |  |
| `withoutDirectories` | object |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /template-message/list` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-template-catalog.md) for the provider-specific parameters and requirements.

