# Umbrella: List Organizations by Email

Finds provider organizations in Umbrella by member email.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-organizations-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-organizations-by-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-organizations-by-email?${params}`, {
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
| `email` | string | no | Email address to look up organization memberships for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountManagerUserId": 1,
      "createdAt": 1,
      "creatorUserId": 1,
      "hasDelegatedAdmin": true,
      "isInternal": true,
      "modifiedAt": 1,
      "mspOrganizationId": 1,
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "organizationTypeId": 1,
      "originId": 1,
      "regionId": 1,
      "resellerId": 1,
      "salesforceAccountId": "string",
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountManagerUserId` | number |  |
| `createdAt` | number |  |
| `creatorUserId` | number |  |
| `hasDelegatedAdmin` | boolean |  |
| `isInternal` | boolean |  |
| `modifiedAt` | number |  |
| `mspOrganizationId` | number |  |
| `organizationId` | number |  |
| `organizationName` | string |  |
| `organizationTypeId` | number |  |
| `originId` | number |  |
| `regionId` | number |  |
| `resellerId` | number |  |
| `salesforceAccountId` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET https://api.umbrella.com/admin/v2/organizations` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations-by-email.md) for the provider-specific parameters and requirements.

