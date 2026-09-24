# ADP: List Business Units

Associate Business Units

```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units?${params}`, {
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
| `filter` | string | no | **Examples:** - /mobileUserAccounts/associateOID eq 'G4O73G9Z62SL2NFM' - /mobileUserAccounts/organizationOID eq 'ABCDEFGH' - /mobileUserAccounts/accountStatusCode eq 'STATCODE' - /mobileUserAccounts/personName/givenName eq 'John' - /mobileUserAccounts/personName/familyName1 eq 'Smith' - /mobileUserAccounts/birthDate eq '01-01-1970' |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `GET hcm/v1/validation-tables/business-units` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-business-units.md) for the provider-specific parameters and requirements.

