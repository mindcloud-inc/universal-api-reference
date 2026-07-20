# Castor EDC: List Survey Package Instances

Retrieves survey package instances from Castor EDC.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-survey-package-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-survey-package-instances?connectionId=$CONNECTION_ID&studyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-survey-package-instances?${params}`, {
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
| `studyId` | string | yes | The Castor study UUID. |
| `participantId` | string | no | Filter results by participant UUID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number to retrieve. |
| `pageSize` | number | no | Page size to retrieve. |
| `ccrPatientId` | string | no | Filter results by CCR patient identifier. |
| `sort` | string | no | Sort field. |
| `dir` | string | no | Sort direction ASC or DESC. |
| `availableFromStart` | string | no | Start of the available_from date range. |
| `availableFromEnd` | string | no | End of the available_from date range. |
| `available` | boolean | no | Filter by whether the survey package instance is currently available. |
| `archived` | boolean | no | Filter by archived status. |
| `repeatable` | boolean | no | Filter mobile survey packages generated from repeatable surveys. |
| `training` | boolean | no | Filter mobile survey packages belonging to training configurations. |
| `status` | string | no | Filter by survey package instance status. |
| `availabilityWindowStart` | string | no | Start of the availability window range. |
| `availabilityWindowEnd` | string | no | End of the availability window range. |
| `finishedOn` | string | no | Filter by finished date. |
| `finishedOnGt` | string | no | Filter by finished date greater than the provided value. |
| `finishedOnGte` | string | no | Filter by finished date greater than or equal to the provided value. |
| `finishedOnLt` | string | no | Filter by finished date less than the provided value. |
| `finishedOnLte` | string | no | Filter by finished date less than or equal to the provided value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/survey-package-instance` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-package-instances.md) for the provider-specific parameters and requirements.

