# Bitly: Update Group Preferences

Updates existing group preferences in Bitly.

```
PUT https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group-preferences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-group-preferences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainPreference` | string | no | The preferred domain setting for the group. |
| `groupGuid` | string | yes | The Bitly group GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domainPreference": "string",
      "groupGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domainPreference` | string |  |
| `groupGuid` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `PATCH /groups/:group_guid/preferences` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-preferences.md) for the provider-specific parameters and requirements.

