# Basecamp: List Recordings

Retrieves recordings from Basecamp.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-recordings?connectionId=$CONNECTION_ID&accountId=6172410&type=Todo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "6172410",
  "type": "Todo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/list-recordings?${params}`, {
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
| `accountId` | string | yes | Basecamp account ID. Example: `6172410`. |
| `type` | list<string> | yes | Recording type to list. One of: `Comment`, `Document`, `Kanban::Card`, `Kanban::Step`, `Message`, `Question::Answer`, `Schedule::Entry`, `Todo`, `Todolist`, `Upload`, `Vault`. Example: `Todo`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | string | no | Single or comma-separated list of project IDs. Accepts multiple values in one string, delimited by `,`. Example: `46425319,46425317`. |
| `status` | list<string> | no | Recording status. One of: `active`, `archived`, `trashed`. |
| `sort` | list<string> | no | Sort field. One of: `created_at`, `updated_at`. |
| `direction` | list<string> | no | Sort direction. One of: `asc`, `desc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/projects/recordings.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recordings.md) for the provider-specific parameters and requirements.

