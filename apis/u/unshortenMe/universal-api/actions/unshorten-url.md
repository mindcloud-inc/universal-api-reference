# Unshorten.Me: Unshorten URL

Retrieves an unshortened destination URL from Unshorten.Me.

```
GET https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unshorten.Me `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fbit.ly%2F3DKWm5t" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://bit.ly/3DKWm5t"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url?${params}`, {
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
| `url` | string | yes | The shortened URL to resolve, such as a bit.ly or TinyURL link. Example: `https://bit.ly/3DKWm5t`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shortened_url": "https://example.com",
      "success": true,
      "unshortened_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shortened_url` | string | The shortened URL that was submitted for resolution. |
| `success` | boolean | Whether Unshorten.Me successfully resolved the submitted URL. |
| `unshortened_url` | string | The resolved destination URL returned by Unshorten.Me. |

## Native endpoint

Through the native Unshorten.Me API, this operation is `GET /api/v2/unshorten` (base URL `https://unshorten.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unshorten-url.md) for the provider-specific parameters and requirements.

