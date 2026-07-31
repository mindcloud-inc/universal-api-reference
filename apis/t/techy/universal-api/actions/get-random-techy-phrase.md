# Techy: Get Random Techy Phrase



```
GET https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Techy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Native Techy JSON response message containing one generated tech-savvy phrase. |

## Native endpoint

Through the native Techy API, this operation is `GET /api/json` (base URL `https://techy-api.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-techy-phrase.md) for the provider-specific parameters and requirements.

