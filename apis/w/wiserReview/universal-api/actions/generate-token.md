# WiserReview: Generate Token

Generates an auth token for WiserReview.

```
GET https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/generate-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiserReview `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/generate-token?connectionId=$CONNECTION_ID&dashboardApiKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardApiKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/generate-token?${params}`, {
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
| `dashboardApiKey` | string | yes | API key from Settings in the WiserReview dashboard. |
| `expiresIn` | number | no | Optional number of days before the generated auth token expires. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authToken": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string | Generated bearer auth token. |
| `message` | string | Provider status message. |
| `success` | boolean | Whether token generation succeeded. |

## Native endpoint

Through the native WiserReview API, this operation is `GET /authToken` (base URL `https://api.wiserreview.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-token.md) for the provider-specific parameters and requirements.

