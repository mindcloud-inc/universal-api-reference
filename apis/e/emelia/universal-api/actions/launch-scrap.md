# Emelia: Launch Scrap

Creates a scrap in Emelia from a Sales Navigator URL.

```
POST https://connect.mindcloud.co/v1/universal/emelia/latest/actions/launch-scrap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/launch-scrap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authes": "string",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/launch-scrap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authes": "string",
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authes` | string | yes | Credential ID list. Provide a JSON array string, for example ["cred_id"]. |
| `name` | string | yes | Scrap name |
| `plannedStart` | string | no | Optional planned start datetime string |
| `url` | string | yes | Source URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createScrap": {}
      },
      "errors": [
        {
          "extensions": {
            "code": "string"
          },
          "locations": [
            {
              "column": 1,
              "line": 1
            }
          ],
          "message": "string",
          "path": [
            "string"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createScrap` | object |  |
| `errors[].extensions.code` | string |  |
| `errors[].locations[].column` | number |  |
| `errors[].locations[].line` | number |  |
| `errors[].message` | string |  |
| `errors[].path[]` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/launch-scrap.md) for the provider-specific parameters and requirements.

