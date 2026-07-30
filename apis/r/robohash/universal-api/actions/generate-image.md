# Robohash: Generate Image



```
GET https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robohash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image?connectionId=$CONNECTION_ID&text=user%40example.com&format=png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "user@example.com",
  "format": "png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image?${params}`, {
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
| `text` | string | yes | Text value used to deterministically generate the Robohash image. Example: `user@example.com`. |
| `format` | list | yes | Image file extension documented by Robohash, such as png or jpg. One of: `bmp`, `jpg`, `png`. Default: `png`. |
| `size` | string | no | Optional image dimensions in WIDTHxHEIGHT format, for example 200x200. Example: `200x200`. |
| `set` | list | no | Optional image set. Official provider documentation and its README list set1 through set6 and any. One of: `any`, `set1`, `set2`, `set3`, `set4`, `set5`, `set6`. |
| `bgset` | list | no | Optional background set. Official public docs list bg1, bg2, or any. One of: `any`, `bg1`, `bg2`. |
| `sets` | string | no | Optional comma-delimited set numbers, for example 1,3. The provider documents explicit set lists as stable compared with set=any. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gravatar` | list | no | Optional Gravatar behavior. Use yes for an email value, or hashed for a pre-hashed email value. One of: `hashed`, `yes`. |
| `ignoreext` | boolean | no | Set to false when the extension should be included in the hashed text value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary image bytes returned by Robohash for the generated image. |
| `type` | string | Runtime buffer type returned for the generated image response. |

## Native endpoint

Through the native Robohash API, this operation is `GET /:text.:format` (base URL `https://robohash.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

