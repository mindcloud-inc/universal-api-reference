# TranslatePlus: Get Supported Languages

Retrieves supported languages and codes from TranslatePlus.

```
GET https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-supported-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-supported-languages?${params}`, {
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
      "supported_languages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `supported_languages` | object |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `GET /v2/supported-languages` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supported-languages.md) for the provider-specific parameters and requirements.

