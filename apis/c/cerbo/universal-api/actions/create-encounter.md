# Cerbo: Create Encounter

Creates a new encounter in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-encounter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-encounter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-encounter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pt_id` | number | no | A valid ID of a non-archived patient. |
| `date_of_service` | date | no | A time stamp (YYYY-MM-DD format preferred) representing the date the encounter took or will take place. Can be future or past. |
| `title` | string | no | The title of the encounter note. |
| `content` | string | no | The plaintext-formatted text of the encounter note. |
| `encounter_type` | string | no | The two-letter abbreviation of the type of encounter note you are creating. |
| `owner` | number | no | A valid ID of a non-archived, non-resource user who is the expected owner/manager of the note. Default is the API “user” itself. |
| `parent_encounter` | number | no | The valid ID of an existing encounter for the designated patient. If set, the new note will be filed as a sub-note of the designated parent encounter. The parent note must belong to the patient set by pt_id and it must not be a sub-note itself. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /encounters` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-encounter.md) for the provider-specific parameters and requirements.

