# SonarQube: Set Default Quality Profile

Updates the default quality profile in SonarQube.

```
PUT https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/set-default-quality-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/set-default-quality-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/set-default-quality-profile', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | SonarQube Web API response payload. |
| `success` | boolean | Whether the operation completed successfully. |

## Native endpoint

Through the native SonarQube API, this operation is `POST /api/qualityprofiles/set_default` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-default-quality-profile.md) for the provider-specific parameters and requirements.

