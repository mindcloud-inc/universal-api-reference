# Streak: List Pipeline Fields

Retrieves pipeline fields from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-fields?connectionId=$CONNECTION_ID&pipelineKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-fields?${params}`, {
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
| `pipelineKey` | string | yes | The key of the pipeline. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "lastUpdatedTimestamp": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | The field key. |
| `lastUpdatedTimestamp` | date | When the field was last updated. |
| `name` | string | The field name. |
| `type` | string | The field type. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/pipelines/:pipelineKey/fields` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-fields.md) for the provider-specific parameters and requirements.

