# TalentLyft: Get Department By External ID

Retrieves a department in TalentLyft by external ID.

```
GET https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-department-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLyft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-department-by-external-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/get-department-by-external-id?${params}`, {
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
| `id` | string | yes | The TalentLyft department external ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLyft API returns.

## Native endpoint

Through the native TalentLyft API, this operation is `GET /v2/departments/:id/external` (base URL `https://api.talentlyft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-department-by-external-id.md) for the provider-specific parameters and requirements.

