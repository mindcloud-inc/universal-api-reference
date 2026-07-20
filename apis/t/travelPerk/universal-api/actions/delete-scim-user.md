# TravelPerk: Delete SCIM User

Deletes an existing SCIM user from TravelPerk.

```
DELETE https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/delete-scim-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/delete-scim-user?connectionId=$CONNECTION_ID&scimUserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scimUserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/delete-scim-user?${params}`, {
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
| `scimUserId` | string | yes | The SCIM user identifier to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TravelPerk API returns.

## Native endpoint

Through the native TravelPerk API, this operation is `DELETE https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scim-user.md) for the provider-specific parameters and requirements.

