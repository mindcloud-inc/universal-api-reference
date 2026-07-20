# Zoho Creator: Get Applications

Retrieves accessible applications from Zoho Creator.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications?${params}`, {
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
      "applications": [
        {}
      ],
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applications` | array<object> | Applications visible to the authenticated Zoho Creator user. |
| `code` | number | Zoho Creator response code. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /meta/applications` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applications.md) for the provider-specific parameters and requirements.

