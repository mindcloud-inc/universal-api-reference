# ShareFile: Create Group



```
POST https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Group": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Group": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Group` | object | yes | The ShareFile group object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": "string",
      "IsShared": true,
      "Name": "Ava Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string | The ShareFile group identifier. |
| `IsShared` | boolean | Whether the returned ShareFile group is shared. |
| `Name` | string | The ShareFile group name. |
| `odata.metadata` | string | The OData metadata URL for the returned group. |
| `odata.type` | string | The OData type for the returned group. |
| `url` | string | The API URL for the returned group. |

## Native endpoint

Through the native ShareFile API, this operation is `POST /Groups` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

