# xMatters: Get subscription share permissions

Retrieves subscription share permissions from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-share-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-share-permissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscription-share-permissions?${params}`, {
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
| `subscriptionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "permissibleActions": {
            "editSubscription": true,
            "subscribe": true,
            "subscribeOthers": true,
            "viewSubscription": true
          },
          "sharedWith": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "shareType": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].permissibleActions.editSubscription` | boolean |  |
| `data[].permissibleActions.subscribe` | boolean |  |
| `data[].permissibleActions.subscribeOthers` | boolean |  |
| `data[].permissibleActions.viewSubscription` | boolean |  |
| `data[].sharedWith.firstName` | string |  |
| `data[].sharedWith.id` | string |  |
| `data[].sharedWith.lastName` | string |  |
| `data[].sharedWith.links.self` | string |  |
| `data[].sharedWith.name` | string |  |
| `data[].sharedWith.recipientType` | string |  |
| `data[].sharedWith.targetName` | string |  |
| `data[].shareType` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET subscriptions/{subscriptionId}/share-permissions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subscription-share-permissions.md) for the provider-specific parameters and requirements.

