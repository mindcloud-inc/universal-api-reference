# CircleCI: Get Project Settings



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native CircleCI API, this operation is `GET /project/:provider/:organization/:project/settings` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-settings.md) for the provider-specific parameters and requirements.

