# Socie: Get Group Membership



```
GET https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-group-membership?connectionId=$CONNECTION_ID&groupIdentifier=string&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupIdentifier": "string",
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-group-membership?${params}`, {
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
| `groupIdentifier` | string | yes | The Socie id or externalId of the group. |
| `identifier` | string | yes | The Socie id or externalId of the group membership. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "id": "string",
      "memberExternalId": "string",
      "memberId": "string",
      "orderNumber": 1,
      "role": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string | The external id for the group membership. |
| `id` | string | The Socie group membership id. |
| `memberExternalId` | string | The external member id linked to the membership. |
| `memberId` | string | The Socie member id linked to the membership. |
| `orderNumber` | number | The display order for the group membership. |
| `role` | string | The role assigned in the group membership. |
| `title` | string | The title for the group membership. |

## Native endpoint

Through the native Socie API, this operation is `GET /api/v1/groups/:groupIdentifier/memberships/:identifier` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-membership.md) for the provider-specific parameters and requirements.

