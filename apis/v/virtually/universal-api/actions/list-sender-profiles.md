# Virtually: List Sender Profiles

Retrieves sender profiles for a platform from Virtually.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-sender-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-sender-profiles?connectionId=$CONNECTION_ID&platformName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platformName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-sender-profiles?${params}`, {
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
| `platformName` | string | yes | The platform name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId/members/senderProfiles/:platformName` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sender-profiles.md) for the provider-specific parameters and requirements.

