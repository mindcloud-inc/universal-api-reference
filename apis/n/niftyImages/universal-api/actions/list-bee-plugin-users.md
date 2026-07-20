# NiftyImages: List Bee Plugin Users

Retrieves Bee Plugin users from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-users?connectionId=$CONNECTION_ID&pluginKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pluginKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-users?${params}`, {
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
| `pluginKey` | string | yes | Bee Plugin key. |
| `startDate` | string | no | Start date in ISO 8601 format. |
| `endDate` | string | no | End date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Images": 1,
      "Opens": 1,
      "Status": "string",
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Images` | number |  |
| `Opens` | number |  |
| `Status` | string |  |
| `UserName` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /BeePlugin/:pluginKey/Users` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bee-plugin-users.md) for the provider-specific parameters and requirements.

