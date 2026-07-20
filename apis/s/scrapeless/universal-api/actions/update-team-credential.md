# Scrapeless: Update Team Credential

Updates an existing team credential in Scrapeless.

```
PUT https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-team-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-team-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "origin": "string",
  "metadata": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-team-credential', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "origin": "string",
    "metadata": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xApiToken` | string | no | API key for authentication |
| `origin` | string | yes | The origin URL (domain) for which these credentials apply |
| `namespace` | string | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `metadata` | object | yes | Updated credential metadata containing authentication data |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Scrapeless API, this operation is `PUT /browser/credentials` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-credential.md) for the provider-specific parameters and requirements.

