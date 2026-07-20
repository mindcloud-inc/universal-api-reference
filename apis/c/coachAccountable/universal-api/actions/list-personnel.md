# CoachAccountable: List Personnel

Retrieves personnel from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-personnel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-personnel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-personnel?${params}`, {
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
| `includeInactive` | boolean | no | Set to true to include Personnel that are marked inactive. Default: `false`. |
| `sortOption` | list | no | One of: `A`, `C`. Default: `C`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "cellPhone": "string",
      "city": "string",
      "CompanyID": 1,
      "companyName": "Ava Chen",
      "country": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homePhone": "string",
      "ID": 1,
      "isActive": true,
      "isRegistered": true,
      "lastLoginDate": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "loginCount": 1,
      "profileExtra": "string",
      "state": "string",
      "workPhone": "string",
      "ZIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `cellPhone` | string |  |
| `city` | string |  |
| `CompanyID` | number |  |
| `companyName` | string |  |
| `country` | string |  |
| `dateAdded` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `homePhone` | string |  |
| `ID` | number |  |
| `isActive` | boolean |  |
| `isRegistered` | boolean |  |
| `lastLoginDate` | date |  |
| `lastName` | string |  |
| `loginCount` | number |  |
| `profileExtra` | string |  |
| `state` | string |  |
| `workPhone` | string |  |
| `ZIP` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-personnel.md) for the provider-specific parameters and requirements.

