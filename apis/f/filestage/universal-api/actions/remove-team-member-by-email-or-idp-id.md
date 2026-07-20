# Filestage: Remove Team Member by Email or IdP ID

Deletes a Filestage team member by email or IdP ID.

```
DELETE https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-team-member-by-email-or-idp-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-team-member-by-email-or-idp-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-team-member-by-email-or-idp-id?${params}`, {
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
| `email` | string | no | Email |
| `idpId` | string | no | The user id in your identity provider |
| `forceRemove` | boolean | no | When set to true, the forceRemove flag ensures the forceful removal of users with Webhooks and API keys. If you attempt to remove a user with Webhooks or API keys without setting the forceRemove flag to true, a 403 Forbidden error will be thrown. Default: `false`. |
| `deleteFromReviews` | boolean | no | When set to true, the member will be removed from the review groups of all projects in this team. If false (default), the member will retain access to reviews they were already part of, even after being removed from the team. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Filestage API returns.

## Native endpoint

Through the native Filestage API, this operation is `DELETE /team/members` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-member-by-email-or-idp-id.md) for the provider-specific parameters and requirements.

