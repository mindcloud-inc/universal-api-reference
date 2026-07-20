# CrowdPower: Update Project Theme

Updates a project theme in CrowdPower.

```
PUT https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project-theme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project-theme" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project-theme', {
  method: 'PUT',
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
| `colorPrimary` | string | no | Primary theme color as a hex code. |
| `colorSidebar` | string | no | Sidebar theme color as a hex code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color_primary": "string",
      "color_sidebar": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color_primary` | string |  |
| `color_sidebar` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `PUT projects/{{credentials.projectId}}/theme` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-theme.md) for the provider-specific parameters and requirements.

