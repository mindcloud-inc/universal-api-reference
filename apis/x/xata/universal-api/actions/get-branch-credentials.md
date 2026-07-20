# Xata: Retrieve branch credentials



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-credentials?connectionId=$CONNECTION_ID&organizationID=string&projectID=string&branchID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-branch-credentials?${params}`, {
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
| `organizationID` | string | yes |  |
| `projectID` | string | yes |  |
| `branchID` | string | yes |  |
| `username` | string | no | Username that the credentials requested for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "password": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `password` | string | Password for accessing the branch database |
| `username` | string | Username for accessing the branch database |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/:projectID/branches/:branchID/credentials` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch-credentials.md) for the provider-specific parameters and requirements.

