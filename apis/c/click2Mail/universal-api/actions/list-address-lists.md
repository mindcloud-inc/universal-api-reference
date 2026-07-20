# Click2Mail: List Address Lists

Retrieves a list of address lists from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-address-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-address-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-address-lists?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numberOfLists` | number | no | number of lists to return |
| `offset` | number | no | offset from beginning to allow you to paginate through the lists |
| `searchkey` | string | no | return only lists where the list name contains the keyword |
| `count` | string | no | Returns a count of the number of lists in a customers account |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "lastUpdated": "string",
      "mappingId": 1,
      "name": "Ava Chen",
      "statistics": {
        "guaranteedDelivery": 1,
        "international": 1,
        "nonmailable": 1,
        "nonstandard": 1,
        "noService": 1,
        "notGuaranteedDelivery": 1,
        "standard": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `lastUpdated` | string |  |
| `mappingId` | number |  |
| `name` | string |  |
| `statistics` | object |  |
| `statistics.guaranteedDelivery` | number |  |
| `statistics.international` | number |  |
| `statistics.nonmailable` | number |  |
| `statistics.nonstandard` | number |  |
| `statistics.noService` | number |  |
| `statistics.notGuaranteedDelivery` | number |  |
| `statistics.standard` | number |  |
| `statistics.total` | number |  |

## Native endpoint

Through the native Click2Mail API, this operation is `GET /molpro/addressLists` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-address-lists.md) for the provider-specific parameters and requirements.

