# Statsig: List Gates

Retrieves gates from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-gates-get-console-v1-gates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-gates-get-console-v1-gates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-gates-get-console-v1-gates?${params}`, {
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
| `idType` | string | no | Filter by idType |
| `type` | string | no | Filter by type |
| `typeReason` | string | no | Filter by typeReason |
| `passRate` | string | no | Filter by pass rate of the gates, as determined by a sampling of overall true/false values returned: 0, 100, or INBETWEEN (pass rate greater than zero but less than 100) |
| `rolloutRate` | string | no | Filter by rollout rate of the gates: 0 (all rules are set to pass 0%), 100 (all rules pass 100% including an "everyone" catch all rule), or INBETWEEN (at least one rule has a pass rate greater than 0 but less than 100) |
| `releasePipelineID` | string | no | Filter by release pipeline ID |
| `teamID` | string | no | Filter by team ID |
| `targetAppID` | string | no | Filter by target app ID |
| `includeArchived` | string | no | Include archived gates in the response |
| `store0100Exposures` | string | no | Filter gates by whether "Store 0/100 Exposures" is enabled. |
| `creatorName` | string | no | Name of the creator. |
| `creatorID` | string | no | ID of the user who created the entity. |
| `tags` | string | no | Filter by tags |
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

Through the native Statsig API, this operation is `GET /console/v1/gates` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-gates-get-console-v1-gates.md) for the provider-specific parameters and requirements.

