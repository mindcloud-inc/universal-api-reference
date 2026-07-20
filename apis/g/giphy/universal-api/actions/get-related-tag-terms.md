# Giphy: Get Related Tag Terms

Retrieves related tag terms from Giphy by term.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-related-tag-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-related-tag-terms?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-related-tag-terms?${params}`, {
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
| `term` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsResponsePayload": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsResponsePayload` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/tags/related/:term` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-tag-terms.md) for the provider-specific parameters and requirements.

