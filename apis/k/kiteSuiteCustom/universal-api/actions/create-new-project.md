# Kite Suite: Create new project



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-project', {
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
| `projectName` | string | no |  |
| `projectType` | string | no |  |
| `projectLead` | string | no |  |
| `avatar` | string | no |  |
| `description` | string | no |  |
| `members[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "description": "string",
      "isFibonacci": true,
      "isTrashed": true,
      "key": "string",
      "labels": [
        "string"
      ],
      "lists": [
        "string"
      ],
      "members": [
        "string"
      ],
      "owner": "string",
      "projectLead": "string",
      "projectName": "Ava Chen",
      "projectPrivacy": "string",
      "projectType": "string",
      "removedMembers": [
        "string"
      ],
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Icon of this project |
| `description` | string | Description of this project |
| `isFibonacci` | boolean | project estimation type series |
| `isTrashed` | boolean | project is trash status |
| `key` | string | Unique key |
| `labels` | array | labels of this project |
| `lists` | array | lists of this project |
| `members` | array | members of this project |
| `owner` | string | userID of creator of this project |
| `projectLead` | string | userId of project leader |
| `projectName` | string | The Name of project |
| `projectPrivacy` | string | The project privacy |
| `projectType` | string | The project type |
| `removedMembers` | array | members of this project |
| `workspace` | string | project belongs to workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/project` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-project.md) for the provider-specific parameters and requirements.

