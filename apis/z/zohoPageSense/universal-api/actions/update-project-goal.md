# Zoho PageSense: Update Project Goal

Updates an existing project goal in Zoho PageSense.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-project-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-project-goal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "projectLinkname": "https://example.com",
  "projectgoal.projectLinkname": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-project-goal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "projectLinkname": "https://example.com",
    "projectgoal.projectLinkname": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `projectLinkname` | string | yes | Project linkname in the path. |
| `projectgoal.displayName` | string | no | Updated goal display name. |
| `projectgoal.projectLinkname` | string | yes | Project linkname inside the request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "projectgoals": [
        {
          "displayName": "Ava Chen",
          "goalId": 1,
          "goalStatus": 1,
          "linkname": "https://example.com",
          "projectLinkname": "https://example.com",
          "success": true
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `projectgoals[].displayName` | string |  |
| `projectgoals[].goalId` | number |  |
| `projectgoals[].goalStatus` | number |  |
| `projectgoals[].linkname` | string |  |
| `projectgoals[].projectLinkname` | string |  |
| `projectgoals[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `PUT /portal/:portalName/projectgoals/:projectLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-goal.md) for the provider-specific parameters and requirements.

