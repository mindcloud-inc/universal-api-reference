# 4HSE: List People

Retrieves people from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-people?${params}`, {
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
| `filter` | object | no | Search filters. |
| `filter.projectId` | string | no | Filter by project ID. |
| `filter.lastName` | string | no | Filter by last name. |
| `filter.code` | string | no | Filter by employee code. |
| `filter.taxCode` | string | no | Filter by tax code. |
| `filter.isEmployee` | number | no | Filter employees only. |
| `history` | boolean | no | Include historicized people. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthDate": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "entityId": "string",
      "firstName": "Ava",
      "isEmployee": 1,
      "isPreventionPeople": 1,
      "lastName": "Chen",
      "ownedActive": true,
      "parentActive": true,
      "personId": "string",
      "projectCountry": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "projectStatus": "string",
      "relatedUser": "string",
      "taxCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthDate` | date |  |
| `code` | string |  |
| `entityId` | string |  |
| `firstName` | string |  |
| `isEmployee` | number |  |
| `isPreventionPeople` | number |  |
| `lastName` | string |  |
| `ownedActive` | boolean |  |
| `parentActive` | boolean |  |
| `personId` | string |  |
| `projectCountry` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `projectStatus` | string |  |
| `relatedUser` | string |  |
| `taxCode` | string |  |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/person/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

