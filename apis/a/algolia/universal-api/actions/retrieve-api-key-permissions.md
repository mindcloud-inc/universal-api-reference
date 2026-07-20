# Algolia: Retrieve API Key Permissions

Retrieves API key permissions and restrictions from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-api-key-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-api-key-permissions?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-api-key-permissions?${params}`, {
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
| `key` | string | yes | API key to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acl": [
        "string"
      ],
      "createdAt": 1,
      "description": "string",
      "validity": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acl` | array<string> |  |
| `createdAt` | number |  |
| `description` | string |  |
| `validity` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/keys/:key` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-api-key-permissions.md) for the provider-specific parameters and requirements.

