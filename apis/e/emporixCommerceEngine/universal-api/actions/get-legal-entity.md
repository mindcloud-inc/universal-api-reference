# Emporix Commerce Engine: Get Legal Entity

Retrieves a legal entity from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-legal-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-legal-entity?connectionId=$CONNECTION_ID&legalEntityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "legalEntityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-legal-entity?${params}`, {
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
| `legalEntityId` | string | yes | The unique ID of the legal entity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountLimit": {},
      "customerGroups": [
        {}
      ],
      "entitiesAddresses": [
        {}
      ],
      "id": "string",
      "legalInfo": {},
      "metadata": {},
      "name": "Ava Chen",
      "parentId": "string",
      "restrictions": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountLimit` | object |  |
| `customerGroups` | array<object> |  |
| `entitiesAddresses` | array<object> |  |
| `id` | string |  |
| `legalInfo` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `parentId` | string |  |
| `restrictions` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /customer-management/{{credentials.tenantId}}/legal-entities/:legalEntityId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-legal-entity.md) for the provider-specific parameters and requirements.

