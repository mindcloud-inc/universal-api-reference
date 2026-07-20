# Clappia: Reorder Section

Updates app section order in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "sourcePageIndex": 1,
  "sourceSectionIndex": 1,
  "targetPageIndex": 1,
  "targetSectionIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/reorder-section', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "sourcePageIndex": 1,
    "sourceSectionIndex": 1,
    "targetPageIndex": 1,
    "targetSectionIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `sourcePageIndex` | number | yes | Zero-based page index containing the section to move. |
| `sourceSectionIndex` | number | yes | Zero-based source section index. |
| `targetPageIndex` | number | yes | Zero-based page index where the section should be moved. |
| `targetSectionIndex` | number | yes | Zero-based target section index. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /appdefinitionv2/reorderSection` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-section.md) for the provider-specific parameters and requirements.

