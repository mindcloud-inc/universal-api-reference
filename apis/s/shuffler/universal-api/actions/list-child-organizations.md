# Shuffler: List Child Organizations

Retrieves child organizations from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-child-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-child-organizations?connectionId=$CONNECTION_ID&parentOrgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parentOrgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-child-organizations?${params}`, {
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
| `cursor` | string | no | Optional pagination cursor. |
| `parentOrgId` | string | yes | Parent Org Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isPartner": true,
      "name": "Ava Chen",
      "regionUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isPartner` | boolean |  |
| `name` | string |  |
| `regionUrl` | string |  |

## Native endpoint

Through the native Shuffler API, this operation is `GET /orgs/{parentOrgId}/suborgs` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-organizations.md) for the provider-specific parameters and requirements.

