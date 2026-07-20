# Easymailing: List Member Activities

Retrieves member activities from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/list-member-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/list-member-activities?connectionId=$CONNECTION_ID&audienceUuid=string&memberUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "audienceUuid": "string",
  "memberUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/list-member-activities?${params}`, {
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
| `audienceUuid` | string | yes | Audience UUID. |
| `memberUuid` | string | yes | Member UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easymailing API returns.

## Native endpoint

Through the native Easymailing API, this operation is `GET /audiences/{{audienceUuid}}/members/{{memberUuid}}/activities` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-member-activities.md) for the provider-specific parameters and requirements.

