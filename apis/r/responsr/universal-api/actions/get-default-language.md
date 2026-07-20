# Responsr: Get Default Language



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-language?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-language?${params}`, {
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
      "cultureName": "Ava Chen",
      "displayName": "Ava Chen",
      "id": 1,
      "nativeName": "Ava Chen",
      "twoLetterCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cultureName` | string |  |
| `displayName` | string |  |
| `id` | number |  |
| `nativeName` | string |  |
| `twoLetterCode` | string |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/languages/default` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-language.md) for the provider-specific parameters and requirements.

