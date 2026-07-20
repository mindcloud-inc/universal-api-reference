# Emelia: Download Scrap

Retrieves a scrap download from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/download-scrap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/download-scrap?connectionId=$CONNECTION_ID&format=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "format": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/download-scrap?${params}`, {
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
| `format` | string | yes | Download format integer. Provide a number such as 0 or 1. |
| `id` | string | yes | Scrap identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "downloadScrap": {}
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
| `data.downloadScrap` | object |  |
| `errors[].extensions.code` | string |  |
| `errors[].locations[].column` | number |  |
| `errors[].locations[].line` | number |  |
| `errors[].message` | string |  |
| `errors[].path[]` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-scrap.md) for the provider-specific parameters and requirements.

