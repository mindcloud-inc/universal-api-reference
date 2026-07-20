# Tarvent: Search Account Entities

Finds account entities in Tarvent by search text.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/search-account-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/search-account-entities?connectionId=$CONNECTION_ID&variables.searchValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.searchValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/search-account-entities?${params}`, {
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
| `variables.searchValue` | string | yes | The text to search across account entities. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityId": "string",
      "entityName": "Ava Chen",
      "entityType": "string",
      "entityTypeName": "Ava Chen",
      "modifiedUtc": "2026-05-07T12:00:00.000Z",
      "parentEntityId": "string",
      "parentEntityName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityId` | string |  |
| `entityName` | string |  |
| `entityType` | string |  |
| `entityTypeName` | string |  |
| `modifiedUtc` | date |  |
| `parentEntityId` | string |  |
| `parentEntityName` | string |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-account-entities.md) for the provider-specific parameters and requirements.

