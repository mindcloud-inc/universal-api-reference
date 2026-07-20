# Survalyzer: Create Members



```
POST https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "panelId": 1,
  "members[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "panelId": 1,
    "members[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenant` | string | no |  |
| `panelId` | number | yes |  |
| `members[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "membersIds": [
        1
      ],
      "validationIssues": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `membersIds` | array<number> | Identifiers of the created panel members. |
| `validationIssues` | array<object> | Validation issues returned while creating members. |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Panel/v3/CreateMembers` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-members.md) for the provider-specific parameters and requirements.

