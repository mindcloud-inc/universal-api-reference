# Agendor: Delete Person

Deletes an existing person from Agendor.

```
DELETE https://connect.mindcloud.co/v1/universal/agendor/latest/actions/delete-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/delete-person?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agendor/latest/actions/delete-person?${params}`, {
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
| `id` | number | yes | ID of the person to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agendor API returns.

## Native endpoint

Through the native Agendor API, this operation is `DELETE /people/:id` (base URL `https://api.agendor.com.br/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-person.md) for the provider-specific parameters and requirements.

