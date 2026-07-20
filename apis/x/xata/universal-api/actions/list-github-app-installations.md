# Xata: List GitHub App installations for organization



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-github-app-installations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-github-app-installations?connectionId=$CONNECTION_ID&organizationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-github-app-installations?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization |

## Response

```json
{
  "success": true,
  "data": [
    {
      "installations": [
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
| `installations` | array<object> | Array of GitHub App installations |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/githubapp/installations` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-github-app-installations.md) for the provider-specific parameters and requirements.

