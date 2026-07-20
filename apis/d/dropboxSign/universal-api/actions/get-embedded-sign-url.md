# Dropbox Sign: Get Embedded Sign URL

Retrieves an embedded signing URL from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-sign-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-sign-url?connectionId=$CONNECTION_ID&signature_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signature_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-sign-url?${params}`, {
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
| `signature_id` | string | yes | The id of the signature to get a sign URL for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dropbox Sign API returns.

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /embedded/sign_url/:signature_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embedded-sign-url.md) for the provider-specific parameters and requirements.

