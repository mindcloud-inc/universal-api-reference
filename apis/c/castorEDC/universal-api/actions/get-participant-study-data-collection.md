# Castor EDC: Get Participant Study Data Collection

Retrieves study data for a participant in Castor EDC.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-participant-study-data-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-participant-study-data-collection?connectionId=$CONNECTION_ID&studyId=string&participantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studyId": "string",
  "participantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-participant-study-data-collection?${params}`, {
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
| `participantId` | string | yes | The participant UUID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldIds` | string | no | Comma-separated list of field UUIDs to include. Accepts multiple values in one string, delimited by `,`. |
| `updatedAfter` | string | no | Only return data points updated strictly after this ISO 8601 timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/participant/:participant_id/data-points/study` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-participant-study-data-collection.md) for the provider-specific parameters and requirements.

