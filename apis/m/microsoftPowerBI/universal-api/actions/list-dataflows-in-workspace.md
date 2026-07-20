# Microsoft Power BI: List Dataflows in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataflows-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataflows-in-workspace?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataflows-in-workspace?${params}`, {
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
| `groupId` | string | yes | The workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuredBy": "string",
      "description": "string",
      "modelUrl": "https://example.com",
      "name": "Ava Chen",
      "objectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuredBy` | string | The dataflow owner. |
| `description` | string | The dataflow description. |
| `modelUrl` | string | A URL to the dataflow definition file. |
| `name` | string | The dataflow name. |
| `objectId` | string | The dataflow ID. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/dataflows` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataflows-in-workspace.md) for the provider-specific parameters and requirements.

