# Stormboard: Update Storm

Updates a Storm in Stormboard.

```
PUT https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-storm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-storm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-storm', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stormId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatars` | string | no | Set to 1 to show user avatars in real time, or 0 to hide them. |
| `description` | string | no | Updated storm description or goals. |
| `ideaCreator` | string | no | Set to 1 to show the idea creator avatar on ideas, or 0 to hide it. |
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |
| `templateId` | string | no | Updated template ID for the storm. |
| `title` | string | no | Updated storm title. |
| `votesPerUser` | string | no | Updated number of votes each user gets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `PUT /storms/:storm_id` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-storm.md) for the provider-specific parameters and requirements.

