# RandomFox: Get Random Fox



```
GET https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RandomFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox?${params}`, {
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
      "image": "string",
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image` | string | Direct URL of the random fox image. |
| `link` | string | RandomFox page URL for the returned image. |

## Native endpoint

Through the native RandomFox API, this operation is `GET /floof/` (base URL `https://randomfox.ca`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-fox.md) for the provider-specific parameters and requirements.

