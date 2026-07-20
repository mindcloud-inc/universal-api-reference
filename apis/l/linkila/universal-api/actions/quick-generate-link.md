# Linkila: Quick Generate Link

Creates a new link and short URL in Linkila.

```
POST https://connect.mindcloud.co/v1/universal/linkila/latest/actions/quick-generate-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/quick-generate-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkila/latest/actions/quick-generate-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetURL` | string | no | Required destination URL for the new Linkila short link. |
| `domainName` | string | no | Optional Linkila domain name for the generated short link. |
| `slug` | string | no | Optional custom slug for the generated short link. |
| `title` | string | no | Optional title for the generated short link. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deepLinkEnabled` | boolean | no | Whether deep-link behavior should be enabled for the generated link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Generated Link record with id, title, defaultDestinationURL, shortUrls, tags, and filterDestinations. |

## Native endpoint

Through the native Linkila API, this operation is `POST /quickGenerate` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quick-generate-link.md) for the provider-specific parameters and requirements.

