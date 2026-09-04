# Acumatica: Search By Entity

Search the 'Default' Acumatica Endpoint for a Specific Entity

```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/search-by-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/search-by-entity?connectionId=$CONNECTION_ID&limit=25&offset=0&entity=Contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "entity": "Contacts"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/search-by-entity?${params}`, {
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
| `entity` | list<string> | yes | The top-level entity to retrieve. Example: "Project" or "User" One of: `Contacts`, `Customer`, `ProFormaInvoice`, `Project`, `ProjectActivity`, `ProjectBudget`, `ProjectEmployee`, `ProjectEquipment`, `ProjectRetainage`, `ProjectTask`, `ProjectTransaction`, `SalesOrder`. |
| `expand` | string | no | Use the expand parameter to specify linked and detail entities that should be expanded. By default, no linked or detail entities are expanded; that is, only fields of the top-level entity are returned. You need to explicitly specify each linked or detail entity to be expanded. (Example: to expand the Project Attributes use $expand=Attributes). Accepts multiple values as an array. |
| `select` | string | no | When you retrieve records from Acumatica ERP you use the $select parameter to specify the fields of the entity to be returned. By default, ALL fields of the entity are returned. Accepts multiple values as an array. |
| `filter` | string | no | Use the $filter parameter to specify conditions that determine which records should be returned from Acumatica ERP. |
| `custom` | string | no | Specify the fields that are not defined in the contract to be returned. For details, see $custom Parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/:entity` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-by-entity.md) for the provider-specific parameters and requirements.

