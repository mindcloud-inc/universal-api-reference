# Openlayer: Get Rule

Retrieves rule details from the Openlayer API.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule?connectionId=$CONNECTION_ID&ruleId=9c409560-3522-4a4f-a6f7-fd06f78c289d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ruleId": "9c409560-3522-4a4f-a6f7-fd06f78c289d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule?${params}`, {
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
| `ruleId` | string | yes | Openlayer rule ID. Default: `9c409560-3522-4a4f-a6f7-fd06f78c289d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "frameworkId": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `frameworkId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /rules/:ruleId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rule.md) for the provider-specific parameters and requirements.

