# Nucleus One: List Organizations

Retrieves organizations available to the current Nucleus One user.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-organizations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Optional continuation cursor returned by a previous list run. Example: `Paste a cursor from a previous response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "ID": "string",
      "Name": "Ava Chen",
      "SubscriptionExpiration": "2026-05-07T12:00:00.000Z",
      "SubscriptionFreeUsers": 1,
      "SubscriptionMinUsers": 1,
      "SubscriptionRequired": true,
      "UniqueBillableOrganizationMembers": 1,
      "UniqueFreeOrganizationMembers": 1,
      "UniqueNonReadOnlyOrganizationMembers": 1,
      "UniqueReadOnlyOrganizationMembers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `ID` | string |  |
| `Name` | string |  |
| `SubscriptionExpiration` | date |  |
| `SubscriptionFreeUsers` | number |  |
| `SubscriptionMinUsers` | number |  |
| `SubscriptionRequired` | boolean |  |
| `UniqueBillableOrganizationMembers` | number |  |
| `UniqueFreeOrganizationMembers` | number |  |
| `UniqueNonReadOnlyOrganizationMembers` | number |  |
| `UniqueReadOnlyOrganizationMembers` | number |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

