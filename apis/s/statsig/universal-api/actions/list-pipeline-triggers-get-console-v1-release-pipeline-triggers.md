# Statsig: List Pipeline Triggers

Retrieves pipeline triggers from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `releasePipelineID` | string | no | Filter by Release Pipeline ID |
| `gateID` | string | no | Filter by Gate ID |
| `dynamicConfigID` | string | no | Filter by Dynamic Config ID |
| `status` | string | no | Filter by Status |
| `startDate` | string | no | Filter by the start date of the date range of the trigger's creation date in UTC, inclusive |
| `endDate` | string | no | Filter by the end date of the date range of the trigger's creation date in UTC, inclusive (i.e. until the end of the day); defaults to today's date if not provided |
| `limit` | number | no | Results per page |
| `page` | number | no | Page number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/release_pipeline_triggers` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pipeline-triggers-get-console-v1-release-pipeline-triggers.md) for the provider-specific parameters and requirements.

