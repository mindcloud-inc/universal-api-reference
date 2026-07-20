# Linkila: Get Redirection

Retrieves a destination URL from Linkila and logs access.

```
GET https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-redirection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-redirection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-redirection?${params}`, {
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
| `shortURL` | string | no | Short URL to resolve. Provide either Short URL or Link ID. |
| `linkId` | string | no | Link ID to resolve. Provide either Short URL or Link ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | string | no | Optional request IP address context for redirection resolution. |
| `headers` | object | no | Optional request headers object for redirection resolution. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "destination_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Resolved redirection response object. |
| `data.destination_url` | string | Destination URL returned for the resolved short link. |

## Native endpoint

Through the native Linkila API, this operation is `POST /redirection` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redirection.md) for the provider-specific parameters and requirements.

