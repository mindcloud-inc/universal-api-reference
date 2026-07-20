# Linkila: Create Redirection Session

Creates a redirection session in Linkila.

```
POST https://connect.mindcloud.co/v1/universal/linkila/latest/actions/create-redirection-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/create-redirection-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortURLId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkila/latest/actions/create-redirection-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortURLId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortURLId` | string | yes | Required Linkila short URL identifier for the redirection session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "session_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created redirection-session response object. |
| `data.session_url` | string | Runtime-observed redirection session URL. Official docs name this as sessionUrl, but runtime returned session_url. |

## Native endpoint

Through the native Linkila API, this operation is `POST /createRedirectionSession` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redirection-session.md) for the provider-specific parameters and requirements.

