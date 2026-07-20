# Murf Dub: List Destination Languages

Retrieves destination languages from Murf Dub.

```
GET https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages?${params}`, {
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
      "language": "string",
      "locale": "string",
      "supports": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string |  |
| `locale` | string |  |
| `supports` | array<string> |  |

## Native endpoint

Through the native Murf Dub API, this operation is `GET /v1/murfdub/list-destination-languages` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-destination-languages.md) for the provider-specific parameters and requirements.

