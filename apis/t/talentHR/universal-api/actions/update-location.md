# TalentHR: Update Location

Updates an existing location in TalentHR.

```
PUT https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectId": 1,
  "name": "Ava Chen",
  "fieldData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectId": 1,
    "name": "Ava Chen",
    "fieldData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectId` | number | yes | Location ID. |
| `name` | string | yes | Location name. |
| `fieldData` | object | yes | Location field data object with address and is_remote. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldData": {},
      "id": 1,
      "name": "Ava Chen",
      "objectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldData` | object |  |
| `id` | number |  |
| `name` | string |  |
| `objectType` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `PUT /locations/:objectId` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

