# Cerbo: List Encounters

Retrieves patient encounters from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounters?connectionId=$CONNECTION_ID&limit=25&offset=0&patient_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "patient_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-encounters?${params}`, {
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
| `patient_id` | number | yes | The ID of the patient. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Limit results to a specific encounter note type (e.g., "ov" for office visit). |
| `signed_only` | boolean | no | If included and set to "false," return all encounter notes, including those not marked as signed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:patient_id/encounters` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-encounters.md) for the provider-specific parameters and requirements.

