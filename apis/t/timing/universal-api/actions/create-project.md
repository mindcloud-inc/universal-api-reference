# Timing: Create Project

Creates a new project in Timing.

```
POST https://connect.mindcloud.co/v1/universal/timing/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timing/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timing/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "color": "string",
      "customFields": {},
      "defaultBillingStatus": "string",
      "isArchived": true,
      "links": {
        "timeEntries": "https://example.com"
      },
      "notes": "string",
      "parent": {
        "self": "string"
      },
      "productivityScore": 1,
      "self": "string",
      "teamId": "string",
      "title": "string",
      "titleChain": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `color` | string |  |
| `customFields` | object |  |
| `defaultBillingStatus` | string |  |
| `isArchived` | boolean |  |
| `links.timeEntries` | string |  |
| `notes` | string |  |
| `parent.self` | string |  |
| `productivityScore` | number |  |
| `self` | string |  |
| `teamId` | string |  |
| `title` | string |  |
| `titleChain` | array<string> |  |

## Native endpoint

Through the native Timing API, this operation is `POST /projects` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

