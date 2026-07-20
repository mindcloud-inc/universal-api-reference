# Xata: Delete a branch



```
DELETE https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-branch?connectionId=$CONNECTION_ID&organizationID=string&projectID=string&branchID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/delete-branch?${params}`, {
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
| `branchID` | string | yes | Unique identifier of the branch to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Xata API, this operation is `DELETE /organizations/:organizationID/projects/:projectID/branches/:branchID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-branch.md) for the provider-specific parameters and requirements.

