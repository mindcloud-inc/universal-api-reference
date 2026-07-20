# Openlayer: Get Framework

Retrieves framework details from the Openlayer API.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework?connectionId=$CONNECTION_ID&frameworkId=29e72db4-dd2f-4331-b1c4-d13b5160a404" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "frameworkId": "29e72db4-dd2f-4331-b1c4-d13b5160a404"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework?${params}`, {
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
| `frameworkId` | string | yes | Openlayer framework ID. Default: `29e72db4-dd2f-4331-b1c4-d13b5160a404`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "enabled": true,
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /frameworks/:frameworkId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-framework.md) for the provider-specific parameters and requirements.

