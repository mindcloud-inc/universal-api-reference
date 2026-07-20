# Xata: Get PostgreSQL configuration details



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-postgres-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-postgres-config?connectionId=$CONNECTION_ID&organizationID=string&projectID=string&branchID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-postgres-config?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project containing the branch |
| `branchID` | string | yes | Unique identifier of the branch to retrieve PostgreSQL configuration for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "parameters": [
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
| `parameters` | array<object> | Array of PostgreSQL configuration parameters with detailed information |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/:projectID/branches/:branchID/postgres-config` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch-postgres-config.md) for the provider-specific parameters and requirements.

