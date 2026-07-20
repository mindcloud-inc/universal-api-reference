# Asana: Add users to a portfolio

Adds users to a portfolio in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-users-to-a-portfolio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-users-to-a-portfolio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataMembers": "string",
  "portfolioGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-users-to-a-portfolio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataMembers": "string",
    "portfolioGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataMembers` | string | yes |  |
| `portfolioGid` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "currentStatusUpdate": {},
      "defaultAccessLevel": "string",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "gid": "string",
      "members": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ],
      "name": "Ava Chen",
      "owner": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "permalinkUrl": "https://example.com",
      "privacySetting": "string",
      "public": true,
      "resourceType": "string",
      "startOn": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | string |  |
| `createdAt` | date |  |
| `createdBy.gid` | string |  |
| `createdBy.name` | string |  |
| `createdBy.resourceType` | string |  |
| `currentStatusUpdate` | object |  |
| `defaultAccessLevel` | string |  |
| `dueOn` | date |  |
| `gid` | string |  |
| `members[].gid` | string |  |
| `members[].name` | string |  |
| `members[].resourceType` | string |  |
| `name` | string |  |
| `owner.gid` | string |  |
| `owner.name` | string |  |
| `owner.resourceType` | string |  |
| `permalinkUrl` | string |  |
| `privacySetting` | string |  |
| `public` | boolean |  |
| `resourceType` | string |  |
| `startOn` | date |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST portfolios/:portfolio_gid/addMembers` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-users-to-a-portfolio.md) for the provider-specific parameters and requirements.

