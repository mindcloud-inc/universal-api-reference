# Agilite: Get Assigned BPM Roles

Retrieves assigned BPM roles from Agilite for a BPM record.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-assigned-bpm-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-assigned-bpm-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-assigned-bpm-roles?${params}`, {
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
| `processKey` | string | no | Optional process key filter for assigned roles. |
| `bpmRecordId` | string | no | Optional BPM record ID filter for assigned roles. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roleNames` | string | no | Optional role name filter; separate multiple role names with commas. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /bpm/getAssignedRoles` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assigned-bpm-roles.md) for the provider-specific parameters and requirements.

