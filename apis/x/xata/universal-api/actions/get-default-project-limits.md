# Xata: Get project resource limits



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-default-project-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-default-project-limits?connectionId=$CONNECTION_ID&organizationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-default-project-limits?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization to get project limits for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "maxBranches": 1,
      "maxDescriptionLength": 1,
      "maxInstances": 1,
      "minInstances": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maxBranches` | number | Maximum number of branches allowed per project |
| `maxDescriptionLength` | number | Maximum character length allowed for project descriptions |
| `maxInstances` | number | Maximum number of database instances allowed per branch |
| `minInstances` | number | Minimum number of database instances required per branch |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/limits` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-project-limits.md) for the provider-specific parameters and requirements.

