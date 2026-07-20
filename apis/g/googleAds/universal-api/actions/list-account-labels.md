# Google Ads: List Account Labels

Retrieves account labels from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-labels?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20label.id%2C%20label.name%20FROM%20label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT label.id, label.name FROM label"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-labels?${params}`, {
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
| `customerId` | list<string> | yes | Customer ID to query (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query for label listing. Default: `SELECT label.resource_name, label.id, label.name, label.status FROM label ORDER BY label.name`. Example: `SELECT label.id, label.name FROM label`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": {
        "id": "string",
        "name": "Ava Chen",
        "resourceName": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label.id` | string |  |
| `label.name` | string |  |
| `label.resourceName` | string |  |
| `label.status` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-labels.md) for the provider-specific parameters and requirements.

