# Datagma: Get Twitter By Email

Retrieves Twitter profile data from Datagma by email.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-twitter-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-twitter-by-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-twitter-by-email?${params}`, {
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
| `email` | string | no | Email address used to look up a Twitter profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "other": {},
      "status": "string",
      "twitter": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `other` | object |  |
| `status` | string |  |
| `twitter` | object |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v1/twitter/by_email` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-twitter-by-email.md) for the provider-specific parameters and requirements.

