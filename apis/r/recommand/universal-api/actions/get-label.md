# Recommand: Get Label

Retrieves a label record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-label?connectionId=$CONNECTION_ID&labelid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-label?${params}`, {
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
| `labelid` | string | yes | labelId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": {
        "colorHex": "string",
        "createdAt": "string",
        "externalId": "string",
        "id": "string",
        "name": "Ava Chen",
        "teamId": "string",
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | object |  |
| `label.colorHex` | string |  |
| `label.createdAt` | string |  |
| `label.externalId` | string |  |
| `label.id` | string |  |
| `label.name` | string |  |
| `label.teamId` | string |  |
| `label.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/labels/:labelId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

