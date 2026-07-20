# Avionte: Query Multiple Talents



```
POST https://connect.mindcloud.co/v1/universal/avionte/latest/actions/query-multiple-talents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/query-multiple-talents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avionte/latest/actions/query-multiple-talents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `talentIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "cellPhone": "string",
      "city": "Ava Chen",
      "companyDepartmentId": 1,
      "companyId": 1,
      "companyName": "Ava Chen",
      "country": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "emailAddress2": "ava@example.com",
      "emailOptOut": true,
      "firstName": "Ava",
      "id": 1,
      "isArchived": true,
      "lastName": "Chen",
      "lastUpdatedDate": "2026-05-07T12:00:00.000Z",
      "latestActivityDate": "2026-05-07T12:00:00.000Z",
      "latestActivityName": "Ava Chen",
      "link": "https://example.com",
      "middleName": "Ava Chen",
      "origin": "string",
      "postalCode": "string",
      "representativeUsers": [
        1
      ],
      "state": "string",
      "status": "string",
      "statusType": "string",
      "title": "string",
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `cellPhone` | string |  |
| `city` | string |  |
| `companyDepartmentId` | number |  |
| `companyId` | number |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdDate` | date |  |
| `emailAddress` | string |  |
| `emailAddress2` | string |  |
| `emailOptOut` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `lastName` | string |  |
| `lastUpdatedDate` | date |  |
| `latestActivityDate` | date |  |
| `latestActivityName` | string |  |
| `link` | string |  |
| `middleName` | string |  |
| `origin` | string |  |
| `postalCode` | string |  |
| `representativeUsers[]` | number |  |
| `state` | string |  |
| `status` | string |  |
| `statusType` | string |  |
| `title` | string |  |
| `workPhone` | string |  |

## Native endpoint

Through the native Avionte API, this operation is `POST front-office/v1/talents/multi-query` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-multiple-talents.md) for the provider-specific parameters and requirements.

