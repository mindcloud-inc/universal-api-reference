# Drag'n Survey: Create Collector Custom Links

Creates respondent identification links for a Drag'n Survey collector.

```
POST https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/create-collector-custom-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Drag'n Survey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/create-collector-custom-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/create-collector-custom-links', {
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
| `collectorId` | string | no | The Drag'n Survey collector ID. |
| `respondents_informations` | string | no | Array of objects to embed into generated authenticated collector links. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Drag'n Survey API returns.

## Native endpoint

Through the native Drag'n Survey API, this operation is `POST collectors/:collectorId/authenticate` (base URL `https://developer.dragnsurvey.com/api/v2.0.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collector-custom-links.md) for the provider-specific parameters and requirements.

