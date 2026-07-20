# Viesus: Get Enhanced Image

Retrieves an enhanced image from Viesus.

```
GET https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-enhanced-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viesus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-enhanced-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-enhanced-image?${params}`, {
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
| `query` | string | no | GraphQL query document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enhancedImage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enhancedImage` | object | Enhanced image details. |

## Native endpoint

Through the native Viesus API, this operation is `POST /` (base URL `https://api.viesus.cloud/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enhanced-image.md) for the provider-specific parameters and requirements.

