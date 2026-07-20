# Castor EDC: Upsert Participant Study Data Collection

Updates participant study data in Castor EDC.

```
PUT https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/upsert-participant-study-data-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/upsert-participant-study-data-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studyId": "string",
  "participantId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/upsert-participant-study-data-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studyId": "string",
    "participantId": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studyId` | string | yes | The Castor study UUID. |
| `participantId` | string | yes | The participant UUID. |
| `data[]` | array<object> | yes | Array of study data point objects with field_id and field_value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `common` | object | no | Optional common parameters object for change_reason and confirmed_changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `POST /study/:study_id/participant/:participant_id/data-points/study` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-participant-study-data-collection.md) for the provider-specific parameters and requirements.

