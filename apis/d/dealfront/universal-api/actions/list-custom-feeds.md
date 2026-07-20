# Dealfront: List Custom Feeds

Retrieves custom feeds from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feeds?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feeds?${params}`, {
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
| `accountId` | number | yes | ID of the account whose custom feeds you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "criteria": [
          {
            "criterionType": "string",
            "displayValue": "string",
            "operator": "string"
          }
        ],
        "name": "Ava Chen"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.criteria[].criterionType` | string |  |
| `attributes.criteria[].displayValue` | string |  |
| `attributes.criteria[].operator` | string |  |
| `attributes.name` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts/:account_id/custom-feeds` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-feeds.md) for the provider-specific parameters and requirements.

