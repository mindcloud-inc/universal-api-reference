# CircleCI: Patch Project Settings



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/patch-project-settings', {
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
| `advanced` | object | no | Advanced project settings payload. |
| `organization` | string | no | VCS organization name. |
| `project` | string | no | Repository name. |
| `provider` | string | no | VCS provider, for example github or bitbucket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advancedSettings": {},
      "organizationName": "Ava Chen",
      "publicKey": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advancedSettings` | object |  |
| `organizationName` | string |  |
| `publicKey` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `PATCH /project/:provider/:organization/:project/settings` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-project-settings.md) for the provider-specific parameters and requirements.

