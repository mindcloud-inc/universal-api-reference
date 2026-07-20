# Outseta: Add Custom Activity

Creates a custom activity in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-custom-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-custom-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-custom-activity', {
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
| `title` | string | no |  |
| `description` | string | no |  |
| `activityData` | string | no |  |
| `entityType` | number | no |  |
| `entityUid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActivityData": "string",
      "Description": "string",
      "EntityType": 1,
      "EntityUid": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivityData` | string |  |
| `Description` | string |  |
| `EntityType` | number |  |
| `EntityUid` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /activities/customactivity` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-activity.md) for the provider-specific parameters and requirements.

