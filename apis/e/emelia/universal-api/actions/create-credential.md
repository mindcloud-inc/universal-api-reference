# Emelia: Create Credential

Creates LinkedIn scraper credentials in Emelia.

```
POST https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cookie": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cookie": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cookie` | string | yes | LinkedIn session cookie |
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
        "scrapCreateAuth": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.scrapCreateAuth` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential.md) for the provider-specific parameters and requirements.

