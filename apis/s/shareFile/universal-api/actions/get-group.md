# ShareFile: Get Group



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-group?${params}`, {
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
| `id` | string | yes | The ShareFile group identifier. |

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

Through the native ShareFile API, this operation is `GET /Groups({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

