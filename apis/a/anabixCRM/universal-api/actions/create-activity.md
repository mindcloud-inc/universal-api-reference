# Anabix CRM: Create Activity

Creates a new activity in Anabix CRM.

```
POST https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.body": "string",
  "data.idContact": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.body": "string",
    "data.idContact": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.body` | string | yes | Activity body. Anabix requires body when creating an activity. |
| `data.idContact` | number | yes |  |
| `data.title` | string | no | Optional activity title. If omitted, Anabix creates a title from the activity body. |
| `data.type` | string | no | Activity type, such as note, call, meeting, email, or SMS. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "customFields": [
        {}
      ],
      "duration": "string",
      "idActivity": 1,
      "idContact": 1,
      "idDeal": 1,
      "revisionInfo": {},
      "timestamp": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `customFields` | array<object> |  |
| `duration` | string |  |
| `idActivity` | number | Anabix activity ID. |
| `idContact` | number |  |
| `idDeal` | number |  |
| `revisionInfo` | object |  |
| `timestamp` | number |  |
| `title` | string | Activity title. |
| `type` | string |  |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

