# Raklet: Delete Contact Phone



```
DELETE https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-phone?connectionId=$CONNECTION_ID&organisationMembershipId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organisationMembershipId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-phone?${params}`, {
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
| `organisationMembershipId` | string | yes | Contact membership identifier in Raklet. |
| `id` | string | yes | Contact phone identifier in Raklet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raklet API returns.

## Native endpoint

Through the native Raklet API, this operation is `DELETE /organisations/:organisationId/contacts/:organisationMembershipId/phones/:id` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-phone.md) for the provider-specific parameters and requirements.

