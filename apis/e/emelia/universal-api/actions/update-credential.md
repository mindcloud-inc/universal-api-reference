# Emelia: Update Credential

Updates LinkedIn scraper credentials in Emelia.

```
PUT https://connect.mindcloud.co/v1/universal/emelia/latest/actions/update-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/update-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cookie": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/update-credential', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cookie": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cookie` | string | yes | LinkedIn session cookie |
| `id` | string | yes | Credential identifier |
| `jsessionid` | string | no | Optional JSESSIONID value |
| `li_a` | string | no | Optional li_at token |
| `ua` | string | no | Optional user agent string |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "scrapUpdateAuth": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.scrapUpdateAuth` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credential.md) for the provider-specific parameters and requirements.

