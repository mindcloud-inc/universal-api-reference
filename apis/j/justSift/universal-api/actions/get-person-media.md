# JustSift: Get Person Media



```
GET https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustSift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person-media?connectionId=$CONNECTION_ID&idOrEmail=ava%40example.com&mediaKind=profile-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "ava@example.com",
  "mediaKind": "profile-photo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justSift/latest/actions/get-person-media?${params}`, {
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
| `idOrEmail` | string | yes | The person's Sift id or email address. |
| `mediaKind` | string | yes | Media kind to retrieve: profile-photo or background-photo. One of: `0`, `1`. Default: `profile-photo`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preferredType` | string | no | Optional profile photo subtype preference: custom or official. One of: `0`, `1`. |
| `height` | number | no | Image height to return, up to 1000. |
| `width` | number | no | Image width to return, up to 1000. |
| `fit` | string | no | Image fit mode: crop or scale. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "idOrEmail": "ava@example.com",
      "mediaKind": "string",
      "size": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Returned image content type. |
| `idOrEmail` | string | Person id or email used for the media request. |
| `mediaKind` | string | Requested media kind. |
| `size` | number | Image response size in bytes. |
| `url` | string | Media request URL. |

## Native endpoint

Through the native JustSift API, this operation is `GET /media/people/:idOrEmail/:mediaKind` (base URL `https://api.justsift.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-media.md) for the provider-specific parameters and requirements.

