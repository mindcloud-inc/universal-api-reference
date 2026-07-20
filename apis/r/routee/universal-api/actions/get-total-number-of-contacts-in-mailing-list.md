# Routee: Get total number of contacts in mailing list

Retrieves total number of contacts in mailing list from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-total-number-of-contacts-in-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-total-number-of-contacts-in-mailing-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-total-number-of-contacts-in-mailing-list?${params}`, {
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
| `id` | string | yes | the ID of the mailing list |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks/:id/emails/total` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-number-of-contacts-in-mailing-list.md) for the provider-specific parameters and requirements.

