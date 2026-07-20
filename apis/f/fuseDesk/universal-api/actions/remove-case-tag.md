# FuseDesk: Remove Case Tag

Removes a tag from an existing FuseDesk case.

```
PUT https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/remove-case-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/remove-case-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseId": 1,
  "caseTagId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/remove-case-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseId": 1,
    "caseTagId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseId` | number | yes |  |
| `caseTagId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v1/cases/:caseId/untag/:caseTagId` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-case-tag.md) for the provider-specific parameters and requirements.

