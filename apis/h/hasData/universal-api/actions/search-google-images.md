# HasData: Search Google Images

Retrieves Google Images results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-images?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-images?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceType` | string | no | Device type for the image search, such as desktop. |
| `ijn` | number | no | Image result page number, where 0 is the first page. |
| `location` | string | no | Google canonical location for the image search. |
| `q` | string | yes | Search query for Google Images. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imagesResults": [
        {}
      ],
      "requestMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imagesResults` | array<object> |  |
| `requestMetadata` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google/images` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-images.md) for the provider-specific parameters and requirements.

