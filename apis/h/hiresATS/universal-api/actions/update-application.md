# 100Hires ATS: Update Application

Updates an existing application in 100Hires ATS.

```
PUT https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "4806315"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "4806315"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Application ID to update. Example: `4806315`. |
| `stageId` | number | no | Optional stage ID to move the application to. Example: `251853`. |
| `isDisqualified` | boolean | no | Mark whether the application is disqualified. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related application resources to include. Example: `candidate,job`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `PUT /applications/:id` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-application.md) for the provider-specific parameters and requirements.

