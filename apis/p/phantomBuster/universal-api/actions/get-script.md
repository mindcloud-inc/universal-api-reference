# PhantomBuster: Get Script

Retrieves a script from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-script?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-script?${params}`, {
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
| `branch` | string | no |  |
| `environment` | list | no | One of: `release`, `staging`. |
| `id` | string | yes | The PhantomBuster script ID to fetch. |
| `withCode` | list | no | One of: `release`, `staging`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessList": [
        "string"
      ],
      "branch": "string",
      "categories": [
        "string"
      ],
      "code": "string",
      "description": "string",
      "environment": "string",
      "id": "string",
      "inputIcon": "string",
      "isDeprecated": true,
      "markdown": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "orgSlug": "string",
      "outputIcon": "string",
      "reservedAgentSlots": 1,
      "reservedAgentSlotsFactor": 1,
      "slug": "string",
      "status": {
        "description": "string",
        "type": "string"
      },
      "unlisted": true,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessList` | array<string> |  |
| `branch` | string |  |
| `categories` | array<string> |  |
| `code` | string |  |
| `description` | string |  |
| `environment` | string |  |
| `id` | string |  |
| `inputIcon` | string |  |
| `isDeprecated` | boolean |  |
| `markdown` | string |  |
| `name` | string |  |
| `orgId` | string |  |
| `orgSlug` | string |  |
| `outputIcon` | string |  |
| `reservedAgentSlots` | number |  |
| `reservedAgentSlotsFactor` | number |  |
| `slug` | string |  |
| `status.description` | string |  |
| `status.type` | string |  |
| `unlisted` | boolean |  |
| `visibility` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /scripts/fetch` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-script.md) for the provider-specific parameters and requirements.

